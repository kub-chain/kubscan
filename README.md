
# KUB Chain Explorer 
<h1 align="center">KUB Chain Explorer (forked from blockscout)</h1>
<h3>Kubscan URL: <a href="https://kubscan.com">kubscan.com</a></h3>
<p align="center">Blockchain Explorer for inspecting and analyzing EVM Chains.</p>
<div align="center">

[![KUB Chain](https://github.com/poanetwork/blockscout/workflows/Blockscout/badge.svg?branch=master)](https://github.com/poanetwork/blockscout/actions) [![Coverage Status](https://coveralls.io/repos/github/poanetwork/blockscout/badge.svg?branch=master)](https://coveralls.io/github/poanetwork/blockscout?branch=master) [![Join the chat at https://gitter.im/poanetwork/blockscout](https://badges.gitter.im/poanetwork/blockscout.svg)](https://gitter.im/poanetwork/blockscout?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

</div>

## About KUBChain Explorer

KUB Chain Explorer is an Elixir application that allows users to search transactions, view accounts and balances, and verify smart contracts on the KUB Chain network including all block data and transactions.

Currently available full-featured block explorers (Etherscan, Etherchain, Blockchair) are closed systems which are not independently verifiable.  As Ethereum sidechains continue to proliferate in both private and public settings, transparent, open-source tools are needed to analyze and validate transactions.

## KUBChain Supported Projects

KUB Chain supports a number of projects. Hosted instances include POA Network, xDai Chain, Ethereum Classic, Sokol & Kovan testnets, and other EVM chains. 

- [List of hosted mainnets, testnets, and additional chains using BlockScout](https://docs.blockscout.com/for-projects/supported-projects)
- [Hosted instance versions](https://docs.blockscout.com/about/use-cases/hosted-blockscout)

## Prerequisites
- Install docker

## Step to run the explorer
1. git clone https://github.com/kub-chain/kubscan.git
2. cd kubscan/
3. run `docker build -f docker/Dockerfile -t kubscan:v2 ../` (will take many minutes to build)
4. run `source env_mainnet.sh` or `source env_testnet.sh`
5. cd docker
6. run a command `make -f Makefile.local start` to start kubscan & postgres container 
7. make sure explorer service is up by run `docker ps` it's will show two containers (blockscout & postgres db)
8. try to access at url: **http://{ip-address}:80** or **http://{domain name}**

## License

[![License: GPL v3.0](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for details.
