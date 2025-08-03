Intro to Fabric
Welcome to Fabric 1.0, the universal decentralized AI execution fabric.
This tutorial introduces you to agent creation, policy enforcement, and royalty-based execution, guiding you through setting up your environment and running your first agent.
🚀 Step 1: Install Fabric CLI
Clone the Fabric CLI repository and build the CLI:
git clone https://github.com/fabric-official/fabric-cli.git
cd fabric-cli
npm install
npm run build
Check the CLI installation:
fab --version
You should see:
Fabric CLI 1.0.0
🔑 Step 2: Configure Wallet
Before deploying agents, configure your developer wallet and network RPC:
fab config set --key <YOUR_PRIVATE_KEY>
fab config set --rpc https://rpc.fabric.network
Verify your configuration:
fab config status
Output example:
Wallet: 0x123...abc
RPC: https://rpc.fabric.network
🧩 Step 3: Create a Simple Agent
Create a .fab file named HelloWorld.fab:
agent HelloWorld
policy {
  payout_split 80% developer, 20% dao
}
execute {
  print("Hello, Fabric!")
}
This agent:
Prints “Hello, Fabric!”
Streams 80% royalties to you, 20% to the DAO treasury
⚡ Step 4: Compile and Run Agent
Compile your agent:
fab build HelloWorld.fab
Run it locally:
fab run HelloWorld
Expected output:
[Agent: HelloWorld] Hello, Fabric!
Policy enforced: ✅
Royalty stream initialized
🌐 Step 5: Deploy to Fabric Network
Deploy your agent to the Fabric registry:
fab agent deploy HelloWorld
Once deployed:
It becomes visible in the agent registry
Other developers can fork it
You start earning royalties on every fork
✅ Next Steps
Fork and Deploy Agents
Join DAO governance to propose changes and vote
Explore advanced tutorials to build more complex agents
