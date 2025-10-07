# AWS EKS Service

This uses a demo build for eks but the steps are basically the same to
deploy any app using AWS eks.

## Action deploy game
The below instructions are for macOS users

- Ensure `kubectl` is installed
- Ensure `Docker` is installed
- Ensure `minikube` is installed for local access
- Connect and install AWS CLI
  - Follow the instructions provided by AWS for installing AWS CLI
- The configure AWS CLI
  - For this you require `access key` and `secret`
  - Create the above from IAM  (Access Management)
    - Users -> Find the specific user and create Access keys

- Type the below command and follow the prompt
```shell
aws configure
```
- For AWS regions, you can find the list [here](https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html)
- Install `eksctl` using `brew`

```shell
brew tap aws/tap
brew install aws/tap/eksctl
```
- Performing zsh completion
```shell
mkdir -p ~/.zsh/completion/
eksctl completion zsh > ~/.zsh/completion/_eksctl
```
- Add to zsh profile
```shell
echo "fpath=($fpath ~/.zsh/completion)" >> ~/.zshrc
```
> [!NOTE]
> If the zsh profile doesn't exist, please create one prior to running the above command
> ```shell
> cd ~/ || exit
> touch .zshrc
>  ```