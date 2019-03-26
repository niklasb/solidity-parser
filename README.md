## Notes (niklasb)

This was constructed as per recommendation from https://github.com/sc-forks/solidity-coverage/issues/316:

1. Install regular solidity-parser-sc package
2. Copy contents from node_modules/solidity-parser-sc
3. Replace build/parser.js by https://raw.githubusercontent.com/maxsam4/solidity-parser/solidity-0.5/build/parser.js


[![Build Status](https://travis-ci.org/ConsenSys/solidity-parser.svg?branch=master)](https://travis-ci.org/ConsenSys/solidity-parser)

## [consensys/solidity-parser](https://github.com/ConsenSys/solidity-parser) with additional project specific grammar rules
For code analysis of contract systems that use custom pre-processsing to deploy or run their tests.

Additions:

**Interpolation (Gnosis)**: 
  + e.g. `{{Variable}}`: used to defer address assignments to contract contructors until
  the contracts' execution context is known.
  ```javascript
  EventFactory constant eventFactory = EventFactory({{EventFactory}});
  address constant marketMaker = {{LMSRMarketMaker}};
  ```
### License

MIT
