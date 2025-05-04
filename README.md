# LPC ("local persistent clipboards")

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/yourusername/project-name.svg)](https://github.com/eddypanther1/LPC)

An adjustable clipboard containing frequntly used sentences or difficult to type symbol

offering local storage to overcome the issue of clipboard getting over-writtaen, 
reducing repetitive typing of same contents saving time
enabling you to focus on the non-repetive portion of your task

![Project Screenshot or Demo](images/screenshot.png)

## Features

- **Local Persistent**: Does not perish after a new copy/paste operation like a clipboard
- **Multiple Editable Clipboards**: Provides multiple quick one-button edit/copy of repetitive contents 
- **Single Press**: For single symbol or short phrase, offers non-editable direct push-button

## Installation

```bash
# Clone the repository
git clone https://github.com/eddypanther1/LPC.git

# Change into the project directory
cd LPC

# Install dependencies
npm install  # or yarn, pip, etc.
```

## Usage

```javascript
// Basic example code showing how to use your project
import { mainFunction } from 'project-name';

const result = mainFunction('example input');
console.log(result);
```


## Configuration

```json
{
  "order": "1",
  "type": "regular",
  "content": "including: frequently, repeatedly, often used phrases"
},
{
  "order": "2",
  "type": "csv_button",
  "content": "😀,✅,⭕,ⓒ,☒,(火),(水)"
},
{
  "order": "3",
  "type": "multimedia",
  "content": "yyyymmddhhss.png"
}


```

## Project Structure

```
LPC/
├── src/             # Source files
├── tests/           # Test files
├── docs/            # Documentation
├── examples/        # Example usage
├── .github/         # GitHub specific files (workflows, templates)
├── LICENSE          # License file
└── README.md        # This file
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Hat tip to anyone whose code was used


## Contact

Eddy Panther -  eddypanther1@gmail.com

Project Link: [https://github.com/eddypanther1/LPC]
