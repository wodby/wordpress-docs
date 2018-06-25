# Deployment 

## Vanilla WordPress (no deployment)

For demo purposes and simple WordPress installations you can use Vanilla WordPress deployment option. In this case WordPress code that comes with the Docker image will be used. In case of changes all data made to your codebase will persist but there will be no versions control.

## Deployment with git

We recommend using [Composer](https://getcomposer.org/) to manage dependencies in your repository:

1. Fork [our boilerplate](https://github.com/wodby/wordpress-composer)
2. Enter `web` in `Codebase dir` input on the 2nd step of new application deployment form

If you're using your own composer template make sure you have `wodby.yml` in the repository root with the following content:

```yml
pipeline:
- name: Install dependencies
  type: command
  command: composer install --no-interaction --optimize-autoloader
  directory: $APP_ROOT
```

## Deployment from CI tool

See https://help.wodby.com/deployment/cicd

## Post-deployment scripts

You can perform some actions such as run a wp cli command after deployment by using [post-deployment scripts](https://help.wodby.com/deployment/post-deployment-scripts)

## Auto deployment via git hooks

See https://help.wodby.com/deployment/auto-deployment-from-git