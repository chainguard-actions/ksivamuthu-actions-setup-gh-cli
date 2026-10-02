# Setup gh cli action

This repo contains the github actions for installing gh cli in self hosted runners. The gh cli is available in the github hosted cloud runners. In self hosted runners, if you want to use the gh cli, you can use this action to install the gh cli. 

## Usage

To install the gh cli, use the actions as below:

   ```yaml
    build:
      runs-on: [self-hosted]
      steps:
        - uses: actions/checkout@v2
        - name: Install the gh cli
          uses: ksivamuthu/actions-setup-gh-cli@<VERSION>
          with:
            version: 2.24.3
        - run: |
            gh version
   ```

## Privacy

This Action contacts Chainguard's licensing server to verify authorization. Connection metadata (IP address, GitHub repository identifier, timestamp, and any metadata encoded in the auth token) is transmitted to Chainguard, Inc. even if authorization is denied in accordance with our [Privacy Notice](https://www.chainguard.dev/legal/privacy-notice)
