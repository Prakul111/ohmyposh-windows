# Oh My Posh

Welcome to the Oh My Posh repository! This repository is dedicated to providing resources and configurations for the Oh My Posh framework. Oh My Posh is a delightful, extensible prompt theme engine for PowerShell. It allows you to customize and enhance your PowerShell prompt with various themes, icons, and styles.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Oh My Posh is designed to make your PowerShell prompt more informative, visually appealing, and tailored to your preferences. With a wide range of themes, icons, and prompt styles to choose from, you can create a personalized prompt that suits your needs and enhances your productivity.

## Features

- **Extensibility**: Oh My Posh is highly extensible, allowing you to create your own themes or customize existing ones to match your preferences.
- **Customization**: Tailor your prompt to your liking by choosing from a variety of icons, prompt segments, colors, and formatting options.
- **Information-rich**: Display relevant information such as the current directory, Git branch, execution time, and more, providing context and aiding your workflow.
- **Compatibility**: Oh My Posh works with both Windows PowerShell and PowerShell Core, ensuring broad compatibility across different PowerShell versions.

## Installation

To install Oh My Posh, follow these steps:

1. Ensure you have PowerShell 5.1 or higher installed on your system.
2. Open a PowerShell terminal.
3. Install the required dependencies:
   - For Windows PowerShell, run the following command:
     ```powershell
     Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
     ```
   - For PowerShell Core, run the following command:
     ```powershell
     Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -ExecutionPolicy Bypass
     ```
4. Install Oh My Posh by running the following command:
   ```powershell
   Install-Module oh-my-posh -Scope CurrentUser
   ```

For detailed installation instructions and troubleshooting, please refer to the [official documentation](https://ohmyposh.dev/docs/installation/).

## Usage

To use Oh My Posh, follow these steps:

1. Open a PowerShell terminal.
2. Run the following command to list the available themes:
   ```powershell
   Get-PoshThemes
   ```
3. Choose a theme you want to use and set it as the active theme:
   ```powershell
   Set-PoshPrompt -Theme <theme-name>
   ```
   Replace `<theme-name>` with the name of the theme you want to use.
4. Your prompt will now reflect the selected theme.

For more detailed usage instructions and configuration options, refer to the [official documentation](https://ohmyposh.dev/docs/usage/).

## Customization

Oh My Posh allows extensive customization to create a prompt that aligns with your personal preferences. To customize your prompt, follow these steps:

1. Open a PowerShell terminal.
2. Run the following command to generate a sample `oh-my-posh.json` configuration file:
   ```powershell
   $themeSettings = Get-PoshThemes | Select-Object -First 1 | Get-ThemeSettings
   $themeSettings | ConvertTo-Json | Out-File oh-my-posh.json
   ```
3. Open the `oh-my-posh.json` file in a text editor and modify the settings as desired. You can change the theme, icons, colors, and other prompt segments.
4. Save the `oh-my-posh

.json` file.
5. Set your customized prompt using the updated configuration:
   ```powershell
   Set-PoshPrompt -ConfigFilePath <path-to-config>
   ```
   Replace `<path-to-config>` with the path to your modified `oh-my-posh.json` file.

For detailed customization instructions and examples, refer to the [official documentation](https://ohmyposh.dev/docs/customization/).

## Contributing

Contributions to this repository are welcome! If you have ideas, improvements, or bug fixes to share, please consider contributing to the project. To contribute, follow these steps:

1. Fork the repository and create a new branch for your contributions.
2. Make your changes and additions, ensuring that the documentation is clear and well-structured.
3. Submit a pull request, describing the changes you made and providing any necessary context.

Please adhere to the repository's [code of conduct](./CODE_OF_CONDUCT.md) and follow the guidelines outlined in the [contribution guide](./CONTRIBUTING.md).

## License

This repository is licensed under the [MIT License](./LICENSE). By contributing to this project, you agree to license your contributions under the same license.
