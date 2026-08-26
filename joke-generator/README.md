# Random Joke Generator 🎭

A simple Node.js application that fetches and displays random jokes from the [JokeAPI](https://jokeapi.dev/).

## Features

- Fetches random jokes from an external API
- Supports both single-line and two-part jokes
- Beautiful formatted console output
- Error handling for API failures
- Easy to extend and customize

## Installation

1. Clone or navigate to this directory
2. Install dependencies:

```bash
npm install
```

## Usage

### Run the joke generator:

```bash
npm start
```

This will fetch and display a random joke in your terminal.

### Development mode with auto-reload:

```bash
npm run dev
```

(Requires `nodemon` to be installed)

## API Information

This project uses the **JokeAPI** (https://jokeapi.dev/) which provides:

- Multiple categories (General, Programming, Knock-knock, etc.)
- Two formats: Single-line or two-part jokes
- No authentication required
- Free to use

### Example Response:

```json
{
  "type": "twopart",
  "setup": "Why don't scientists trust atoms?",
  "delivery": "Because they make up everything!",
  "category": "General",
  "flags": { "nsfw": false, "religious": false }
}
```

## Project Structure

```
joke-generator/
├── index.js          # Main application logic
├── package.json      # Project dependencies
└── README.md         # This file
```

## Customization

You can modify `index.js` to:

- Filter jokes by category (e.g., 'Programming', 'Knock-Knock')
- Set specific joke types
- Add your own joke sources
- Store jokes in a database
- Create a web interface

Example - fetch programming jokes only:

```javascript
const response = await axios.get('https://v2.jokeapi.dev/joke/Programming', {
  params: {
    type: 'any',
    format: 'json'
  }
});
```

## License

MIT

## Contributing

Feel free to fork, modify, and improve this project!
