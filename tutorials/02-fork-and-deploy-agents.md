Fork and Deploy Agents

In Fabric 1.0, forking agents is the foundation of developer monetization and ecosystem growth.
This tutorial teaches you how to:
Find existing agents
Fork and modify them
Deploy your fork
Start earning perpetual royalties

🔍 Step 1: Discover Existing Agents
List available agents in the Fabric registry:
fab agent list
Example output:
ID     NAME           FORKS  ROYALTY_SPLIT
001    HelloWorld     10     80/20
002    DataCleaner    5      75/25

🧩 Step 2: Fork an Agent
Fork the HelloWorld agent:
fab agent fork 001 --name MyForkedAgent
Output:
[✔] Agent forked successfully!
New Agent ID: 003
Name: MyForkedAgent
Royalty Split: 80% to you, 20% to original developer

✍️ Step 3: Modify the Forked Agent
Open the forked .fab file:
agent MyForkedAgent
policy {
  payout_split 80% developer, 20% dao
}
execute {
  print("This is my improved HelloWorld agent!")
}

⚡ Step 4: Compile and Test
Compile your fork:
fab build MyForkedAgent.fab
Run it locally:
fab run MyForkedAgent
Output:
[Agent: MyForkedAgent] This is my improved HelloWorld agent!
Policy enforced: ✅

🌐 Step 5: Deploy Forked Agent
Deploy to Fabric network:
fab agent deploy MyForkedAgent
Output:
[✔] Agent deployed successfully
Registry ID: 003
Royalty stream activated

💰 Step 6: Claim Royalties
Whenever your fork is used or forked again:
fab claim
Output:
Claiming royalties...
New Royalty Payment: 15.2 FAB
Total Claimed: 120 FAB

🔑 Key Benefits of Forking
Immediate royalties for your fork
Original developer also earns (collaborative economy)
Network effect: every fork strengthens DAO treasury

✅ Next Steps
DAO Governance
Propose improvements to agent economics
Participate in DAO votes to shape Fabric’s evolution
