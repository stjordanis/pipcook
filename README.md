# Pipcook

A JavaScript application framework for machine learning and its engineering.

<a href="https://www.npmjs.com/package/@pipcook/pipcook-core">
  <img alt="npm" src="https://img.shields.io/npm/dm/@pipcook/pipcook-core"></a>
<a href="https://www.npmjs.com/package/@pipcook/pipcook-core">
  <img alt="npm" src="https://img.shields.io/npm/v/@pipcook/pipcook-core"></a>
<a href="https://github.com/alibaba/pipcook/actions">
  <img alt="Github Action Build" src="https://github.com/alibaba/pipcook/workflows/build/badge.svg?branch=master&event=push"></a>
<a href="https://hub.docker.com/r/pipcook/pipcook">
  <img alt="Docker Cloud Build Status" src="https://img.shields.io/docker/cloud/build/pipcook/pipcook"></a>
<a href="https://github.com/alibaba/pipcook">
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/alibaba/pipcook"></a>
<a href="https://opensource.org/licenses/Apache-2.0">
  <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"></a>

## Why Pipcook

With the mission of enabling JavaScript engineers to utilize the power of machine learning without any
prerequisites and the vision to lead front-end technical field to the intelligention. [Pipcook][] is to become
the JavaScript application framework for the cross-cutting area of machine learning and front-end interaction.

We are truly to design Pipcook's API for front-end and machine learning applications, and focusing on the front-end
area and developed from the JavaScript engineers' view. With the principle of being friendly to JavaScript, we will 
push the whole area forward with the machine learning engineering. For this reason we opened an issue about 
[machine-learning application APIs][], and look forward to you get involved.

## What's Pipcook

Pipcook can be divided into the following 3 layers from top to bottom.

__Pipcook Application__

It defines flexible and intuitive APIs to build machine-learning application, even though you don't know the details 
of algorithm.

__Pipcook Core__

It's used to represent ML pipelines consisting of Pipcook plugins. This layer ensures the stability and scalability 
of the whole system, and uses a plug-in mechanism to support rich functions including: dataset, training, validations
and deployment.

__Pipcook Bridge to Python__

For JavaScript engineers, the most difficult part is the lack of a mature machine learning toolset in the ecosystem.
To this end, we have opened up the interaction between Python and Node.js at the bottom and can easily call some 
missing APIs.

## Quick start

### Setup

Prepare the following on your machine:

| Installer   | Version range |
|-------------|---------------|
| [Node.js][] | >= 12     |
| [Python][]  | >= 3.6        |
| [npm][]     | >= 6.1        |

Install the command-line tool for managing [Pipcook][] projects:

```shell
$ npm install -g @pipcook/pipcook-cli
```

Initialize a project:

```sh
$ mkdir pipcook-example && cd pipcook-example
$ pipcook init
```

### Playground
If you are wondering what you can do in [Pipcook][] and where you can check your training logs and models, you could start from Pipboard

```sh
$ pipcook board
```

You will see a web page prompt in your browser, and there is a MNIST showcase on the home page and play around there. If you want to train a model to recognize MNIST handwritten digits by yourself, you could try the examples below.

- [pipeline-mnist-image-classification][]: pipeline for classific Mnist image classification problem.
- [pipeline-databinding-image-classification][]: pipeline example to train the iamge classification task which is 
  to classifify [imgcook](https://www.imgcook.com/) databinding pictures.
- [pipeline-object-detection][]: pipeline example to train object detection task which is for component recognition 
  used by imgcook.
- [pipeline-text-bayes-classification][]: pipeline example to train text classification task with bayes

See [here](./example) for complete list, and it's easy and quick to run these examples. For example, to do a MNIST 
image classification, just run the following to start the pipeline:

```sh
$ pipcook run examples/pipelines/mnist-image-classification.json
```

__NOTICE__: the last two examples are using Boa (pipcook python bridge layer). 
Before run them, you need to setup Python environment. See [here](docs/tutorials/want-to-use-python.md) for more information

## Documentation

Please refer to [English](docs/) | [中文](docs/zh-cn/)

## Developers

Clone this repository:

```sh
$ git clone git@github.com:alibaba/pipcook.git
```

Install [lerna][] and [TypeScript][], and check:

```sh
$ lerna -v
$ tsc -v
```

install dependencies, e.g. via [npm][]:

```sh
$ npm install
```

After the above, now build the project:

```sh
$ npm run build
```

- Developer Documentation [English](./docs/devel/developer-guide.md) | [中文](./docs/zh-cn/devel/developer-guide.md)
- [Project Guide](./docs/meta/PROJECT_GUIDE.md)
- [Roadmap, 2020](https://github.com/alibaba/pipcook/issues/30)

## Community

#### IRC

<img width="200" src="./community_qrcode.png">

> Download DingTalk (an all-in-one free communication and collaboration platform) here: [English](https://www.dingtalk.com/static/en/download) | [中文](https://page.dingtalk.com/wow/dingtalk/act/download)

#### Who's using it

<a href="https://www.imgcook.com"><img height="40" src="https://img.alicdn.com/tfs/TB1lle4yQzoK1RjSZFlXXai4VXa-200-64.png"></a>
## License

[Apache 2.0](./LICENSE)

[Pipcook]: https://github.com/alibaba/pipcook
[lerna]: https://github.com/lerna/lerna
[TypeScript]: https://github.com/microsoft/TypeScript
[Node.js]: https://nodejs.org/
[npm]: https://npmjs.com/
[Python]: https://www.python.org/
[machine-learning application APIs]: https://github.com/alibaba/pipcook/issues/33
[pipeline-mnist-image-classification]: example/pipelines/mnist-image-classification.json
[pipeline-databinding-image-classification]: example/pipelines/databinding-image-classification.json
[pipeline-object-detection]: example/pipelines/object-detection.json
[pipeline-text-bayes-classification]: example/pipelines/text-bayes-classification.json
