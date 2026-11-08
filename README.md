# Serverless - Build Frontend to call API Gateway

> Calling Amazon API Gateway from a front end.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000079-CallAPI/

## Overview

In the last post, we know how to create and use Lambda functions that interact with S3 and DynamoDB. Next in this series, we build a web application (front-end) to interact with the database through Lambda and API Gateway.

## Workshop contents

1. Introduction API Gateway / DynamoDB
2. Front-end deployment
3. Deploy Lambda function
   - Create DynamoDB table
   - Deploy Lambda function
4. Config API Gateway
   - Create methods
   - Setting and enable CORS
5. Test APIs by Postman
6. Test APIs with front-end
7. Clean up

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone https://github.com/vanhoangkha/000079-CallAPI.git
cd 000079-CallAPI
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Complete the **Clean up** chapter when you finish to remove them.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
