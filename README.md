# Learn platform

In progress material for <https://docs.polygon.technology/innovation-design/>,
to be rebranded as Learn. Content managed by the
[Polygon Devrel team](https://polygon.technology/community/meet-the-devrel).

## Content

External contributors should feel at home grabbing some of the incomplete topics
and sending in PRs with drafts. If you run into a tutorial about Polygon's tech
stack in the wild that isn't mentioned here, please feel free to
[open an issue](https://github.com/0xPolygon/devrel-docs/issues) or
[contact us](https://polygon.technology/community/meet-the-devrel) to discuss
adding it.

### Getting your feet wet

- General Concepts
  - [x] The Polygon stack: Clarifying the choice
- Agglayer
  - [x] Overview
  - [x] Trust Levels Between AggLayer Chains
  - [ ] Learn AggLayer: A comprehensive list of external resources
  - [x] A day in the life of an AggLayer tx
  - [x] Pessimistic Proof
  - [x] Unified Liquidity
  - [ ] Block building in Agglayer
  - [ ] Network parameters and contract addresses
  - [ ] Detailed look at AggLayer L1 contracts
- PoS
  - [ ] Overview
  - [ ] A Day in the Life of a Polygon PoS TX
  - [ ] Block building in Polygon PoS
  - [ ] Network parameters and contract addresses
  - [ ] Detailed Look at Polygon PoS L1 Contracts
  - [ ] Let’s deploy a contract to Polygon PoS!
  - [ ] The gas costs implications of advanced contracts
- zkEVM
  - [ ] Overview
  - [ ] A Day in the Life of a Polygon zkEVM TX
  - [ ] Block building in Polygon zkEVM
  - [ ] Network parameters and contract addresses
  - [ ] Detailed Look at Polygon zkEVM L1 Contracts
  - [ ] Let’s deploy a contract to Polygon zkEVM!
  - [ ] The gas costs implications of advanced contracts and L1 settlements
- Miden Basic
  - [ ] Overview
  - [ ] A Day in the Life of a Miden TX
  - [x] Note Types
  - [ ] Block building in Miden
  - [ ] Network parameters
  - [ ] Miden Use Cases
  - [ ] Writing Miden Contracts
    - [ ] Miden Assembly Crash Course 1: Hello World
    - [ ] Miden Assembly Crash Course 2: Counter
    - [ ] Miden Rust Crash Course
    - [ ] Deploying to Production
    - [ ] Coinflip Step by Step
    - [ ] Rock Paper Scissors Step by Step

### Going for a swim

A section for those who passed the basics of dapp development on the Polygon
stack and are ready to take full advantage of some Polygon stack USPs.

- Miden advanced
  - [ ] Deep dive into Miden architecture
  - [ ] Advanced contract development techniques
  - [ ] Call logic across multiple notes
  - [ ] Developing multi-contract dapps
  - [ ] Using Miden for privacy-preserving applications
  - Advanced dApp development
    - [ ] Let’s build a private-voting DAO step-by-step
    - [ ] Ensuring security and privacy: implications and tradeoffs
- AggLayer
  - [ ] Chaining cross-chain calls with `BridgeAndCall`
  - [ ] CCIP vs AggLayer for cross chain calls
  - [ ] Sequencing: centralization tradeoffs and future solutions
  - Gaming supercase
    - [ ] Simple game design
    - [ ] Simple marketplace on Polygon PoS
    - [ ] Characters on Polygon zkEVM
    - [ ] Equipping game items across chains with `BridgeAndCall`

### Deep dive

- Plonky3
  - [ ] Into Plonky3
  - [ ] How to choose your own configuration for Plonky3
  - [ ] Your first AIR circuits and implementation, Fibonacci Example on Plonky3
- CDK
  - [ ] Kurtosis CDK
  - [ ] Validium vs Calldata Rollup
  - [ ] The issue of EIP4844 (blob) support
  - [ ] Launching your own L2
  - [x] [Launching your own L2 with Presto](https://blog.jarrodwatts.com/build-your-own-layer-2-blockchain-using-polygon-cdk)
  - [x] [Quick and dirty DAC integration with your chain](https://docs.polygon.technology/cdk/how-to/integrate-da/)
  - [ ] L2 + setting up a whitelisted DAC
  - [ ] L2 + setting up an open and incentive-driven DAC
  - [ ] Going bare metal
    - [ ] Launching each part of the Kurtosis CDK separately
    - [ ] …
    - [ ] …

### 🏆 Buildooors

- [ ] Shipper directory
- [ ] Quickswap case study
- [ ] Shipper A case study
- [ ] Shipper B case study
- [ ] …

---

## Community

Join our community in the [R&D Discord](https://discord.gg/0xpolygonrnd), or
schedule a meet with us at
[Meet the Dev Rel](https://polygon.technology/community/meet-the-devrel).

Additionally, we have a [YouTube channel](https://www.youtube.com/@0xPolygonTV)
and a [Polygon blog](https://polygon.technology/blog).

Long-form persisted discussions happen in the
[Developer Forum](https://forum.polygon.technology/).

## Contributing

The process below will help you run the docs locally.

### Repo Translations

- [x] English
- [ ] Chinese
- [ ] Thai

Please [get in touch](https://polygon.technology/community/meet-the-devrel) if
you want to help translate this into other languages.

### Prerequisites

1. [Python 3.12](https://www.python.org/downloads/).
2. Install [`virtualenv`](https://pypi.org/project/virtualenv/):

```sh
pip3 install virtualenv
```

### Setup

1. Clone the repository to your local machine.
2. Navigate to the root directory of the cloned repository:

   ```sh
   cd devrel-docs
   ```

3. Ensure the `serve_docs.sh` script is executable by running:

   ```sh
   chmod +x serve-docs.sh
   ```

4. To serve the documentation, run the following command:

   ```sh
   ./serve_docs.sh
   ```

5. Once the script executes, the documentation site will be accessible at:
   <http://127.0.0.1:8000/>.

If it runs and renders well here, it will render correctly on the Knowledge
Layer. If there are any unfixed errors breaking the local build, it will
probably break on import to the Knowledge Layer.

## Commands

- `mkdocs new [dir-name]` - Create a new project.
- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build the documentation site.
- `mkdocs -h` - Print help message and exit.

### Linting

There is a linting script at `./prettier.sh` which you can run if you have
Prettier installed. The `.prettierrc` file is used to configure Prettier and
should work with most modern IDEs and build processes.
