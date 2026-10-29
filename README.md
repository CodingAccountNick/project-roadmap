# Project Roadmap

This is what I'm building and what I plan to build next. Each project lists its goal, tech stack, planned features and current status.

| Project | Area | Status |
|---|---|---|
| [Shipment Assistant](#shipment-assistant) | AI / Backend | 🟡 In progress ([repo](https://github.com/CodingAccountNick/shipment-assistant)) |
| [AWS Serverless Infrastructure with Terraform](#aws-serverless-infrastructure-with-terraform) | Cloud / DevOps | ✅ First version done ([repo](https://github.com/CodingAccountNick/aws-serverless-terraform)) |

---

## Shipment Assistant

An AI assistant that answers questions about shipments in plain language: where a package is, when it will arrive, and why it's delayed.

**Repo:** [CodingAccountNick/shipment-assistant](https://github.com/CodingAccountNick/shipment-assistant)

**Tech stack:** Python, FastAPI, Ollama (Llama 3.2, run locally), .NET (Visual Studio solution, planned)

**Done so far**
- [x] Script that sends a question to a locally hosted Llama 3.2 model and returns its answer

**Planned**
- [ ] REST API (FastAPI) with typed request and response models
- [ ] Connect the model to real shipment data so its answers are based on actual records
- [ ] Web chat interface
- [ ] Docker setup for running the API and the model together

---

## AWS Serverless Infrastructure with Terraform

Infrastructure as code for a serverless backend on AWS, built from reusable Terraform modules.

**Repo:** [CodingAccountNick/aws-serverless-terraform](https://github.com/CodingAccountNick/aws-serverless-terraform)

**Tech stack:** Terraform, AWS (Lambda, IAM, S3), Node.js, GitHub Actions

**Done so far**
- [x] Remote Terraform state stored in S3
- [x] Reusable module for the IAM role that Lambda functions run under
- [x] Reusable Lambda module, used to deploy an auth handler written in Node.js
- [x] GitHub Actions pipeline that runs `terraform init`, `fmt -check`, `validate` and `plan` on every push to `main`, with AWS credentials kept in GitHub Secrets

**Next steps**
- [ ] API Gateway in front of the Lambda functions
- [ ] Authentication with Amazon Cognito
- [ ] Separate dev and prod environments
- [ ] Add a manually approved `apply` step to the CI pipeline

---

## Contact

- GitHub: [@CodingAccountNick](https://github.com/CodingAccountNick)
