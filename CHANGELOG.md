# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Changed
- Change tokenizer from tokenizers by HuggingFace to original SentencePiece tokenizer
### Fixed
- Generation algorithm for chatlm which caused by replacing tokenizer to SentencePiece


## [v0.4.0] - 2020/08/01
### Added
- Tokenizer trainer to train your customized tokenizer
### Fixed
- Bad word filter which did not filter out bad ids because of the filtering order of top_k-top_p and bad_word filters
### Changed
- Adopting generate function providing by HuggingFace instead of own implementation
- Dropped MeCab+BPE based tokenizer and adopt SentencePiece based custom tokenizer instead

## [v0.3.1] - 2020/06/25

### Added

- Implement bad_words option to chatlm.generator
- Implement response argument to chatlm.generator

## [v0.3.0] - 2020/06/21

### Changed

- Removed PyTorch dependency and introduced Tensorflow intead
- Introduced YAML config for configuration of model hyperparameters

### Removed

- Removed papermill dependency; adopted CLI with YAML config file instead of papermill

## [v0.2.0] - 2020/04/29

### Added

- Introduced jupyternotebook executed with Papermill.
- Implemented ChatLM model which is a simple sequence to sequence model using GPT-2.
- Implemented TopPKGenerator to specify both top-p and top-k filtering.

### Removed

- Removed ChatModel. This model will be implemented in the future, but currently it has some bugs. So this model is removed from current version.

## [v0.1.2] - 2020/02/14

### Fixed

- Remove all special tokens from generated text to extract response.

## [v0.1.1]

### Added

- Add license file.

### Changed

- Fix vocab_size and num_albels in the BaseModel training script to adapt Transformers from v2.2.0 to v2.3.0.

## v0.1.0

### Added

- Add scripts for BaseModel and ChatModel.
