<p align="center">
  <img alt="Blaxel Logo" src="https://blaxel.ai/logo_short.png" height="140" />
  <h3 align="center">Blaxel Action</h3>
  <p align="center"><a href="https://github.com/features/actions">GitHub Action</a> for Blaxel</p>
  <p align="center">
    <a href="https://github.com/beamlit/bl-action/releases/latest"><img alt="GitHub release" src="https://img.shields.io/github/release/beamlit/bl-action.svg?logo=github&style=flat-square"></a>
    <a href="https://github.com/marketplace/actions/bl-action"><img alt="GitHub marketplace" src="https://img.shields.io/badge/marketplace-blaxel--action-blue?logo=github&style=flat-square"></a>
  </p>
</p>

---

- [Usage](#usage)
  - [Workflow](#workflow)
- [Setup](#setup)
- [License](#license)
- [Contributing](#contributing)
- [Support](#support)

## Usage

[Blaxel](https://www.blaxel.ai) is a platform for building and deploying AI agents. Please visit [the documentation](https://docs.blaxel.ai) for more information about Blaxel.
With this action, you can automate the deployment of your AI resources to Blaxel directly from your GitHub workflows.

### Workflow

```yaml
name: Deploy to Blaxel
on: [push]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Deploy to Blaxel
        uses: beamlit/blaxel-action@v1
        with:
          workspace: "your-workspace"
          apikey: ${{ secrets.BL_API_KEY }}
          deploy: "path/to/your/deployment/folder"
```

## Setup

1. **Create a Blaxel API Key**: Go to your Blaxel account settings and generate an API key.
2. **Add the API Key to GitHub Secrets**: In your GitHub repository, navigate to Settings > Secrets and add a new secret named `BL_API_KEY`.
3. **Configure the Workflow**: Use the example above to configure your GitHub Actions workflow file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Support

For any questions or issues, please open an issue in this repository.
