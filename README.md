<p align="center">
  <img alt="Beamlit Logo" src="https://beamlit.com/logo_short.png" height="140" />
  <h3 align="center">Beamlit Action</h3>
  <p align="center"><a href="https://github.com/features/actions">GitHub Action</a> for Beamlit</p>
  <p align="center">
    <a href="https://github.com/beamlit/beamlit-action/releases/latest"><img alt="GitHub release" src="https://img.shields.io/github/release/beamlit/beamlit-action.svg?logo=github&style=flat-square"></a>
    <a href="https://github.com/marketplace/actions/beamlit-action"><img alt="GitHub marketplace" src="https://img.shields.io/badge/marketplace-beamlit--action-blue?logo=github&style=flat-square"></a>
  </p>
</p>

___

* [Usage](#usage)
  * [Workflow](#workflow)
* [Setup](#setup)
* [License](#license)
* [Contributing](#contributing)
* [Support](#support)

## Usage

[Beamlit](https://www.beamlit.com) is a platform for building and deploying AI agents. Please visit [the documentation](https://docs.beamlit.com) for more information about Beamlit.
With this action, you can automate the deployment of your AI resources to Beamlit directly from your GitHub workflows.

### Workflow

```yaml
name: Deploy to Beamlit
on: [push]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Deploy to Beamlit
        uses: beamlit/beamlit-action@v1
        with:
          workspace: 'your-workspace'
          apikey: ${{ secrets.BEAMLIT_API_KEY }}
          deploy: 'path/to/your/deployment/folder'
```

## Setup

1. **Create a Beamlit API Key**: Go to your Beamlit account settings and generate an API key.
2. **Add the API Key to GitHub Secrets**: In your GitHub repository, navigate to Settings > Secrets and add a new secret named `BEAMLIT_API_KEY`.
3. **Configure the Workflow**: Use the example above to configure your GitHub Actions workflow file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Support

For any questions or issues, please open an issue in this repository.
