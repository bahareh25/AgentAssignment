Riverbend Bike Share AI Agent

A small AI-powered service assistant built with .NET 10, C#, Microsoft.Agents.AI, Microsoft.Extensions.AI, and Foundry Local.

Features
Find bike-share stations by name
Retrieve service reports using station IDs
AI tool calling with IChatClient
Session-based conversation context
Structured AI output with validation
Local AI model execution
Technologies
.NET 10
C#
Microsoft.Agents.AI
Microsoft.Extensions.AI
Microsoft.AI.Foundry.Local
xUnit
Qwen 2.5 1.5B
Tools
find_station

Finds a station by name using case-insensitive, partial matching.

get_service_reports

Returns service reports for a station using its station ID.

Project Structure
AgentAssignment.App
├── Contracts
├── MyStationData
├── MyStationPack
├── MyAssistantFactory
└── ModelSetup
Run

Build the project:

dotnet build

Run the application:

dotnet run

Generate the local-model transcript:

dotnet run -- transcript

Run tests:

dotnet test
Local Model

The project uses Foundry Local with:

qwen2.5-1.5b

The model runs locally, providing the AI capabilities without requiring a cloud deployment.

Testing

The project includes offline tests for seed data, tools, contracts, and agent functionality.

Model-dependent live tests require a configured AI model.

Security

Do not commit secrets, API keys, credentials, model files, bin/, or obj/ folders to the repository.
