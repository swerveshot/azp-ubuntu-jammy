# Ubuntu 22.04 LTS (Jammy Jellyfish) Docker container for Azure Pipelines agent.

[![CI](https://github.com/swerveshot/azp-ubuntu-jammy/workflows/Build/badge.svg?branch=main&event=push)](https://github.com/swerveshot/azp-ubuntu-jammy/actions?query=workflow%3ABuild) [![Docker pulls](https://img.shields.io/docker/pulls/swerveshot/azp-ubuntu-jammy)](https://hub.docker.com/r/swerveshot/azp-ubuntu-jammy/)

Created from build instructions on Microsoft Azure DevOps documentation as can be found here: https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops

## How to Use
Use these environment variables to run the agent.

### Environment variables
| Environment variable | Description                                                 |
|----------------------|-------------------------------------------------------------|
| AZP_URL              | The URL of the Azure DevOps or Azure DevOps Server instance. |
| AZP_TOKEN            | [Personal Access Token (PAT)](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops) with **Agent Pools (read, manage)** scope, created by a user who has permission to [configure agents](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/pools-queues?view=azure-devops#create-agent-pools), at `AZP_URL`.    |
| AZP_AGENT_NAME       | Agent name (default value: the container hostname).          |
| AZP_POOL             | Agent pool name (default value: `Default`).                  |
| AZP_WORK             | Work directory (default value: `_work`).                     |
| TARGETARCH           | Defines the CPU architecture of the target. Select between `linux-x64` (default), `linux-arm64` or `linux-arm`. |
