# GPTPromptKit 📚

**Get Format DATA(Like JSON) from GPT!**
GPTPromptKit is a library that helps developers interact with AI language models more effectively by using prompt engineering techniques. The library offers several techniques that can be used depending on the situation, improving the clarity and accuracy of prompts, and enabling more effective communication with users.

repo: [gpt-prompt-kit](https://github.com/clean99/gpt-prompt-kit)

## Features 🎁

1. **Translate** 🌐 : Ask questions in a clear and concise manner to improve translation accuracy.
2. **Format (Text Normalization)** 📝: Use a specific format to prompt the user with two available options:
    - **JSON**: Provide a JSON schema and input, and receive output in this format.
    - **Free**: Specify any desired format and receive output accordingly.
3. **ChainOfThought** 🤔: Prompt GPT to think through the problem step by step.(Coming soon)

## Installation 📦

Install GPTPromptKit using npm:

```
npm install gpt-prompt-kit
```


## Usage 🚀

Create a new file named `index.js` and add the following code:

```javascript
import { GPTPromptKit, gptPromptKitFactory } from 'gpt-prompt-kit';

// custom your prompt function to create a gPTPromptKit instance.
const prompt = (text) => {
  // Your function to send the text to GPT and receive a response
};

const gptPromptKit = new GPTPromptKit(prompt);

// or you can just pass API_KEY to use the build-in GPT-3.5 model

const gptPromptKit = gptPromptKitFactory(API_KEY);

// Example usage:
// Translate
const translate = gptPromptKit.translate(Lang.English, Lang.Chinese);
translate('Hello, world!').then(console.log);

// Format JSON
const formatJson = gptPromptKit.formatJson({ key: 'explain it', key2: 'explain it' });
formatJson('Description here', { key: 'example' }).then(console.log);

// Format Free
const formatFree = gptPromptKit.formatFree('Any format template you want');
formatFree('Description here').then(console.log);

```

## Demo 🥸

In demo directory there are some use demo for you to test the abilities of this library.

To use those demo:

1. Install dependencies:

```
npm install
```

2. Compile & Run the demo:

```
tsc demo/translate.ts
node demo/translate.js
```

### Translate

![translator](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/translate.png "translator")
![translator](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/translate2.png "translator")

### Format JSON

You can get a JSON string with any fields you want:

![formatJson](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/formatJSON.png "formatJson")
![formatJson](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/formatJSON2.png "formatJson")

### Format Free

![formatFree](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/formatFree.png "formatFree")
![formatFree](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/formatFree2.png "formatFree")

## Changelog 📝

### 1.1.1
- delete interpreter so that browser also can use this library.
- add customize option for gptPromptKitFactory. Now we can use different GPT model.
![customizedOptions](https://github.com/clean99/gpt-prompt-kit/blob/main//demo-img/customizedOptions.png "customizedOptions")

## Development 🛠️

To contribute to GPTPromptKit, follow these steps:

1. Clone the repository and install dependencies:

```
git clone https://github.com/clean99/gpt-prompt-kit.git
cd gpt-prompt-kit
npm install
```

2. Build the project:

```
npm run build
```

3. Test the project:

```
npm test
```

4. Lint the project:

```
npm run lint
```

5. Format the project:

```
npm run format
```

## Contributing 🤝
We welcome contributions to GPTPromptKit! If you'd like to contribute, please fork the repository, create a new branch, make your changes, and submit a pull request.

## License 📄
GPTPromptKit is licensed under the [MIT License](/LICENSE).

```

Feel free to modify the code snippets, installation, usage, and contributing sections as necessary to match your library's actual implementation and requirements.
```
