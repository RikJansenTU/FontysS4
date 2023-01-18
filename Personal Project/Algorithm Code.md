# Algorithm Code
Some C# code that 'rates' a sentence based on a number of characteristics.    
    
    // See https://aka.ms/new-console-template for more information
    using System.Text.Json;
    using Newtonsoft.Json.Linq;

    Console.WriteLine("Input your sentence:");
    string sentence = Console.ReadLine();
    Console.WriteLine(Algorithm.RateSentence(sentence));

    internal class Algorithm
    {
        //Returns a one-word rating of a sentence (to later corespond to LEDs on the device)
        public static string RateSentence(string sentence)
        {
            if (AverageWordLength(sentence) < 5)
                return "Simplistic";
            if (AnalyseSentenceRarity(sentence) > 1)
                return "Derivative";
            if (ContainsSpecialWord(sentence))
                return "Groundbreaking";
            if (AnalyseAlliteration(sentence) > 2)
                return "Worthwhile";
            return "Amateurish";
        }

        //returns the average number of characters that words in the sentence consist of
        static double AverageWordLength(string sentence)
        {
            string[] words = sentence.Split(' ');
            List<int> wordLength = new();
            foreach (string word in words)
            {
                wordLength.Add(word.Length);
            }
            return wordLength.Average();

        }

        //returns the relative frequency of a word in 1 million words 
        static async Task<double> AnalyseWordRarity(string word)
        {
            using HttpClient client = new();
            client.DefaultRequestHeaders.Accept.Clear();

            double result = 0;

            try
            {
                string responseBody = await client.GetStringAsync($"https://api.datamuse.com/words?sp={word}&md=f&max=1");

                //Doesn't work since right now since I switched to a different API
                //JObject o = JObject.Parse(responseBody);
                //var parsedObject = JsonDocument.Parse(responseBody);
                //var frequencyString = parsedObject.RootElement.GetProperty("tags");*/

                result = 0;
            }
            catch (HttpRequestException e)
            {
                Console.WriteLine("Something went wrong");
                Console.WriteLine("Message: " + e.Message);
            }
            return result;
        }

        //returns the average frequency of words in the sentence
        static double AnalyseSentenceRarity(string sentence)
        {
            string[] words = sentence.Split(' ');
            List<double> wordScores = new();

            foreach (string word in words)
            {
                double score = AnalyseWordRarity(word).Result;
                wordScores.Add(score);
            }
            return wordScores.Average();
        }

        //checks if the sentence contains one of an array of predefined words
        static bool ContainsSpecialWord(string sentence)
        {
            string[] specialWords = { "antedeluvian", "metaphorical", "sesquipedalian", "supine", "serendipity" };
            string[] words = sentence.Split(' ');
            foreach (string word in words)
            {
                if (specialWords.Contains(word)) return true; 
            }
            return false;
        }

        //returns the largest succession of words in a sentence that start with the same letter
        static int AnalyseAlliteration(string sentence)
        {
            string[] words = sentence.Split(' ');

            char previousLetter = '0';
            int result = 0;
            int count = 0;

            for (int i = 0; i < words.Length; i++)
            {
                //check if the first letter of the word matches with the first letter of the previous word
                if (words[i][0] == previousLetter)
                {
                    count++;
                } else
                {
                    if (count > result) 
                        result = count;
                }
                previousLetter = words[i][0];
            }

            return result;
        }
    }
