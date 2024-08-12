# GenAI Video Short-form Generator

This repository is a sample generative AI video short-form generator application that uses Amazon Bedrock, Amazon Transcribe orchestrated with AWS serverless services.
This sample application takes in long videos, understands it, and extracts and generate up to 15 short-form highlight video. 
It uses distant parts from the video to make more than 10 engaging, short-form content with titles and subtitles.
The app also gives flexibility in choosing which frame to put in, and also the ability to edit titles and subtitles auto-generated by LLMs. 

https://github.com/user-attachments/assets/0dc48322-9d61-4e16-8381-13ae3083fa7e

## Deployment

### Prerequisites

1. Install [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) & Set up [AWS credentials](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)

2. Install [AWS CDK](https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html#getting_started_install) & CDK [Bootstrap](https://docs.aws.amazon.com/cdk/v2/guide/bootstrapping-env.html#bootstrapping-howto) (for the first time)

3. [Manage Model Access](https://docs.aws.amazon.com/bedrock/latest/userguide/model-access.html)

> [!IMPORTANT]
> - The application uses Amazon Bedrock in the **us-west-2** region. Please allow model access in **us-west-2**.
> - The application only supports models from Anthropic Claude 3.0 and above **(3.0 Haiku, 3.0 Sonnet, 3.0 Opus, 3.5 Sonnet)**.

### Sandbox Deployment

1. Clone repository

```sh
git clone https://github.com/aws-samples/gen-ai-video-short-form-generator.git
```

2. Install dependencies

```sh
cd gen-ai-video-short-form-generator
npm install
```

3. Deploy cloud sandbox

```sh
npx ampx sandbox
```

> [!IMPORTANT]
> - It takes about 10 minutes to deploy.
> - Do not terminate the sandbox environment while running the front-end application.

4. Run frontend app

```sh
npm run dev
```

### Amplify Deployment

Create your own repository and follow [Amplify deployment steps](https://docs.amplify.aws/react/start/quickstart/#2-deploy-the-starter-app)

## Clean Up

### Sandbox Environment

```sh
npx ampx sandbox delete
```

> [!IMPORTANT]
> You can verify whether all the resources have been deleted in the AWS CloudFormation console.

### Amplify Development

To delete an Amplify project that has been deployed from the Amplify Development Step, 

1. Go to your Amplify project console
2. Navigate to `App Settings > General Settings > Delete app`

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## Contacts

- [Kihoon Kwon](https://github.com/kyoonkwon)
- [Sukwon Lee](https://github.com/ltrain81)


## License

This library is licensed under the MIT-0 License. See the [LICENSE](LICENSE) file.

## Open Source Library

For detailed information about the open source libraries used in this application, please refer to the [ATTRIBUTION](ATTRIBUTION.md) file.
