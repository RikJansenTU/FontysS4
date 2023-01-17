This code sometimes adds a stylistic modifier to the prompts, so if the prompts was 'airplane' it might turn it into 'airplane, psychedelic art'. The styles I chose are based on my experimentation with DALL-E to see which ones consistently produced the most interesting results.

	const generateImages = async prompt => {
		setPrompts([]) // rest image prompts

		// generate similar & opposite prompts
		const similarPrompt = []
		const oppositePrompt = []
		for (const word of prompt.split(' ')) {
			const words = await getSynonymAndAntonym(word)
			similarPrompt.push(words[0] ?? word)
			oppositePrompt.push(words[1] ?? word)
		}

		// add random artstyles
		prompt += generateStyle();
		similarPrompt.join(' ');
		similarPrompt += generateStyle();
		oppositePrompt.join(' ');
		oppositePrompt += generateStyle();

		// shuffle prompts
		setPrompts(shuffle([prompt, similarPrompt, oppositePrompt]))
	}

	function generateStyle() {
		const result = '';

		// random chance for a stylistic indicator to be added
		const i = Math.floor(Math.random() * 2);
		if (i < 1) {
			return result;
		}
		// determines what stylistic effect gets added
		else {
			i = Math.floor(Math.random() * 6);
			switch (i) {
				case 1:
					result += ', watercolor art';
					break;
				case 2:
					result += ', psychedelic art';
					break;
				case 3:
					result += ', cartoon art';
					break;
				case 4:
					result += ', bauhaus art';
					break;
				case 5:
					result += ', low poly art';
					break;
				default: break;
			}
			return result;
        }
    }
