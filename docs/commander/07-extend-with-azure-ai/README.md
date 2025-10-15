# 🚨 Mission 07: Extend agents with Azure AI

## 🕵️‍♂️ CODENAME: `OPERATION AZURE INTELLIGENCE`

> **⏱️ Operation Time Window:** `~60 minutes`  

## 🎯 Mission Brief

Your agent is powerful on its own, but connecting it to Azure AI unlocks enterprise-grade capabilities. This mission will teach you how to use Azure AI Foundry and Azure AI Search to create intelligent, custom experiences that go beyond out-of-the-box functionality.

By mission's end, you'll have deployed a custom AI model in Azure AI Foundry, integrated it into your agent through custom prompt actions, created a searchable knowledge base in Azure AI Search, and connected it all to your agent for expanded knowledge and capabilities.

## 🔎 Objectives

In this mission, you'll learn:

1. Understanding what Bring Your Own Model (BYOM) and Bring Your Own Data (BYOD) mean in the context of Microsoft Copilot Studio
1. Learning why and when to use BYOM and BYOD capabilities with your agents
1. Exploring how BYOM and BYOD integrate with Copilot Studio agents
1. Deploying AI models in Azure AI Foundry and connecting them via custom prompt actions
1. Creating searchable indexes in Azure AI Search and using them as knowledge sources

## 🤖 What does Bring Your Own Model mean?

Bring Your Own Model (BYOM) allows you to use custom or third-party AI models with your Copilot Studio agents instead of relying solely on the models built into Copilot Studio. This gives you flexibility to choose specialized models that best fit your specific use case. With BYOM, you can choose a model for your agent that meets your specific needs.

### What does BYOM enable?

- **Custom AI capabilities** - use specialized models trained for specific domains like legal, medical, or financial services.
- **Model flexibility** - select from various model providers including Azure OpenAI, open-source models, or your own fine-tuned models.
- **Control and compliance** - maintain control over model selection, deployment location, and data handling to meet regulatory requirements.
- **Cost optimization** - choose models that balance performance with cost based on your workload requirements.

### Types of models you can bring

- **Azure OpenAI models** - GPT-4, GPT-3.5, and other models deployed in your Azure subscription.
- **Azure AI model catalog** - access 1900+ models from the extensive Azure AI Foundry model catalog.
- **Custom fine-tuned models** - models you've trained or fine-tuned on your specific data.
- **Open-source models** - popular models like Llama, Mistral, or Phi deployed in Azure.

## 📊 What does Bring Your Own Data mean?

Bring Your Own Data (BYOD) enables you to connect your own enterprise data sources to your Copilot Studio agents, allowing them to provide grounded, accurate responses based on your organization's information.

### What does BYOD enable?

- **Enterprise knowledge** - ground your agent's responses in your organization's documents, databases, and systems.
- **Accurate information** - reduce hallucinations by connecting to authoritative data sources.
- **Real-time data** - access current information from your systems rather than relying on pre-trained knowledge.
- **Contextual responses** - provide answers that are relevant to your organization's specific context and terminology.

### Types of data sources you can bring

- **Azure AI Search** - searchable indexes of documents, websites, and structured data.
- **SharePoint** - documents and files stored in SharePoint sites.
- **OneDrive** - files stored in OneDrive for Business.
- **Dataverse** - structured data from your Power Platform environment.
- **Custom connectors** - any data source accessible via API.

## 🎯 Why use BYOM and BYOD in Microsoft Copilot Studio agents?

While Copilot Studio provides powerful out-of-the-box capabilities, BYOM and BYOD unlock advanced scenarios that make your agents truly enterprise-ready.

### Reasons to use BYOM

1. **Specialized expertise**
    - Use domain-specific models that understand industry terminology and context better than general-purpose models.
    - Example: a medical terminology model for healthcare agents.

1. **Performance optimization**
    - Select smaller, faster models for simple tasks and larger models for complex reasoning.
    - Balance response time with capability requirements.

1. **Compliance and governance**
    - Deploy models in specific Azure regions to meet data residency requirements.
    - Maintain full control over model versions and updates.

1. **Cost management**
    - Use cost-effective models for high-volume, low-complexity interactions.
    - Reserve premium models for complex scenarios.

1. **Custom capabilities**
    - Leverage models fine-tuned on your organization's data and use cases.
    - Implement specialized capabilities not available in standard models.

### Reasons to use BYOD

1. **Accuracy and reliability**
    - Ground responses in authoritative enterprise data rather than general knowledge.
    - Reduce the risk of hallucinations and incorrect information.

1. **Current information**
    - Access real-time data from your systems.
    - Ensure users receive up-to-date information.

1. **Enterprise context**
    - Provide responses that understand your organization's terminology, processes, and policies.
    - Reference internal documents, guidelines, and knowledge bases.

1. **Compliance**
    - Keep sensitive data within your environment rather than sending it to external services.
    - Maintain audit trails of data access.

1. **Personalization**
    - Tailor responses based on user roles, departments, or permissions.
    - Surface relevant information from the right data sources.

## ⚙️ How BYOM and BYOD work in Microsoft Copilot Studio agents

Understanding how these capabilities integrate with your agent helps you design effective solutions.

### BYOM integration architecture

1. **Model deployment**
    - Deploy your chosen model in Azure AI Foundry.
    - Configure the model endpoint and authentication.

1. **Connection in Copilot Studio**
    - Create a custom prompt action or generative action.
    - Connect to your Azure AI Foundry model endpoint.
    - Configure input parameters and output handling.

1. **Agent invocation**
    - Your agent calls the custom action during conversation.
    - Passes user input and context to the model.
    - Receives and processes the model's response.

1. **Response handling**
    - Parse the model output.
    - Format and present results to the user.
    - Handle errors and fallback scenarios.

### BYOD integration architecture

1. **Data preparation**
    - Index your data in Azure AI Search.
    - Configure field mappings and search capabilities.
    - Set up semantic ranking for improved relevance.

1. **Knowledge source configuration**
    - Add Azure AI Search as a knowledge source in Copilot Studio.
    - Configure authentication and index selection.
    - Define how results should be presented.

1. **Query processing**
    - Agent receives user query.
    - Searches your indexed data for relevant information.
    - Ranks and retrieves top results.

1. **Response generation**
    - Agent uses retrieved data to generate grounded responses.
    - Provides citations and sources to users.
    - Handles cases where no relevant data is found.

### Integration patterns

**Pattern 1: Custom prompt actions with BYOM**

- Use custom prompt actions to call your deployed model.
- Pass specific instructions and user input to the model.
- Receive structured or unstructured responses.
- Best for: specialized processing, custom analysis, domain-specific tasks.

**Pattern 2: Generative actions with BYOM**

- Create actions that combine your model with dynamic inputs.
- Enable the agent to adapt behavior based on conversation context.
- Support multi-step reasoning and complex workflows.
- Best for: multi-turn conversations, complex decision-making, adaptive responses.

**Pattern 3: Knowledge sources with BYOD**

- Configure Azure AI Search as a knowledge source.
- Enable automatic searching during conversations.
- Provide cited, grounded responses to user queries.
- Best for: FAQ handling, document search, information retrieval.

**Pattern 4: Combined BYOM + BYOD**

- Use your custom model to process results from your data sources.
- Enhance retrieval with custom ranking or filtering logic.
- Generate personalized responses based on retrieved data.
- Best for: complex enterprise scenarios, personalized experiences, advanced analytics.

## 🔌 Key capabilities and considerations

### Model capabilities

- **Prompt engineering** - craft effective prompts that guide model behavior.
- **Context management** - pass relevant conversation history and context to the model.
- **Token optimization** - manage input and output token usage for cost efficiency.
- **Error handling** - implement robust error handling for model failures.

### Data capabilities

- **Semantic search** - leverage AI-powered search for better relevance.
- **Hybrid search** - combine keyword and semantic search for comprehensive results.
- **Filtering** - apply filters based on user permissions, departments, or categories.
- **Ranking** - use custom ranking profiles to surface the most relevant results.

### Security and governance

- **Authentication** - secure connections to Azure AI services using managed identities or API keys.
- **Data privacy** - ensure sensitive data remains within your environment.
- **Access control** - implement role-based access to models and data sources.
- **Monitoring** - track usage, performance, and costs across all integrations.

## 🎨 Best practices

1. **Start with use cases**
    - Identify specific scenarios where BYOM or BYOD adds value.
    - Don't over-engineer - use built-in capabilities when they're sufficient.

1. **Choose the right model**
    - Match model capabilities to your use case requirements.
    - Consider cost, latency, and performance trade-offs.

1. **Prepare your data**
    - Ensure data is well-structured and properly indexed.
    - Use semantic ranking for better search relevance.
    - Keep indexes updated with fresh content.

1. **Optimize prompts**
    - Test and refine prompts for your custom models.
    - Include clear instructions and examples.
    - Manage token usage efficiently.

1. **Handle failures gracefully**
    - Implement fallback logic when models or data sources are unavailable.
    - Provide helpful error messages to users.
    - Log issues for monitoring and troubleshooting.

1. **Monitor and optimize**
    - Track usage patterns and costs.
    - Optimize model selection and data retrieval strategies.
    - Continuously improve based on user feedback.

## 🧪Lab 7.1: BYOD from AI Search to your agent

### Prerequisites to complete this mission

1. An active Azure subscription with permissions to create resources

1. Access to [Azure AI Foundry](https://ai.azure.com) through your Azure account

1. Sample documents from [IT policies](https://download-directory.github.io/?url=https://github.com/RobStand/agent-academy/tree/main/docs/commander/07-extend-with-azure-ai/assets/it-documentation&filename=commander_sampledata).

1. [HR policy training data](./assets/hr-policies/hr_policy_training_data.jsonl)

First we will set up an AI Search index for the IT policies. You'll use this index as a knowledge source in Copilot Studio later.

### 7.1.1 Create AI Foundry resources

1. Navigate to [Azure AI Foundry](https://ai.azure.com) and sign in with your Azure credentials.
    ![Navigate to AI Foundry](./assets/7-navigate-ai-foundry.png)

1. Once you are logged in, navigate to [All resources](https://ai.azure.com/allResources) in AI Foundry.

    Select **Create new**. Choose `AI hub resource` and select **Next**.
    ![Create new AI hub resource](./assets/7-create-ai-hub-resource.png)

1. Name your project `commander-workshop`. Rename the hub `commander-hub`. Expand **Advanced options** if you want to specify options, such as a specific resource group name. For this lab, you can accept the defaults.

    Select **Create**.
    ![Create AI Foundry project](./assets/7-create-ai-foundry-project.png)

### 7.1.2 Add the IT policies to AI Foundry

Now you will add the IT policy documents to Azure AI Foundry.

1. In **Azure AI Foundry**, in the left navigation, select **Data + indexes**.

    ![Select data and indexes](./assets/7-data-indexes.png)

1. Select the **Data files** tab.

    Select **+ New data**.

1. Select `Upload files/folders` in the **Data source** dropdown.

1. Select `Upload files or folder`, then `Upload files`.

1. Navigate to the folder containing the IT policy documents, select all of files, and select **Open**.

    Select **Next**.

    ![Upload documents](./assets/7-add-documents-data.png)

1. Enter `it-policies-guides` in **Data name**.

    Select **Create**.

1. The documents are now uploaded to AI Foundry and ready to be used.

    ![Uploaded documents](./assets/7-uploaded-data.png)

### 7.1.3 Create the index

1. In **Azure AI Foundry**, in the left navigation, select **Data + indexes**.

    Select the **Indexes** tab.

    Select **+ New index**.

    ![Select data and indexes](./assets/7-add-index.png)

1. The **Create a vector index** window will load. This is where you will configure the index in AI Foundry.

   In the **Data source** dropdown, choose `Data in Azure AI Foundry`.

1. Select the `it-policies` folder.

    Select **Next**.

1. Now you need to create an Azure AI Search service to ingest your data. Select **Create a new Azure AI Search resource**.

1. The Azure portal will open in a new window and display **Create a search service**.

    Enter the details.

    **Subscription** - The subscription you're using for this lab

    **Resource group** - The resource group you created for the AI Foundry project

    **Service name** - Enter a unique name for the service

    **Location** - Select a region where you created your AI Foundry project or another region near you

    **Pricing tier** - Select `Basic`. The free tier does not include semantic ranking

    Select **Review + create**, then **Create**.

    ![Enter AI Search service details](./assets/7-ai-search-configuration.png)

1. Wait for the connection to complete (1-2 minutes). You'll see a confirmation message.

    ![Connection complete](./assets/7-search-service-complete.png)

1. The AI Search resource is now available. Now is a good time to take note of the search service endpoint URL and the API key. You'll need these when you add AI Search as a knowledge source in Copilot Studio.

    Select **Go to resource**.

    The endpoint URL is displayed under **Essentials**.

    The admin keys are in **Settings** → **Keys**.

1. Go back to AI Foundry to select the AI Search service you created. In the **Select Azure AI Search service** dropdown, select **Connect other Azure AI Search resource**.

1. In the **Connect an existing resource** window, you will see the Azure AI Search resource you created. Select **Add connection** next to the resource.

    ![Connect existing AI Search resource](./assets/7-connect-existing-resource.png)

1. In the **Select Azure AI Search service** dropdown, select your AI Search service.

1. For **Vector index**, enter `it-policies-index`.

    Select **Next**.

1. An embedding model is required for the vector index. In the **Embedding model** dropdown, choose `text-embedding-3-small`. This is a good, low cost embedding model for this scenario.

    Select **Next**.
    ![Configure search settings](./assets/7-configure-search-settings.png)

1. Select **Create vector index**. The indexing process will begin automatically and may take a while.

    ![Indexing complete](./assets/7-index-complete.png)

Excellent work! You've successfully created an Azure AI Search index with vector embeddings. Your IT policy documents are now searchable and ready to be used as a knowledge source for your Copilot Studio agent.

### 7.1.4 Add Azure AI Search as knowledge source

Now you'll connect your AI Search index as a knowledge source for your agent.

1. In your agent, select the **Knowledge** tab in the navigation bar. Select **+ Add knowledge**.

1. Select **Azure AI Search**. Select the dropdown under **Your connections** and select **Create new connection**

1. Configure the connection:

    - **Authentication type**: Access key
    - **Azure AI Search Endpoint URL**: Your AI Search service endpoint URL
    - **Azure AI Search Admin Key**: Your AI Search service admin key

    ![Configure AI Search connection](./assets/7-configure-ai-search-connection.png)

1. Select **Create**. You'll see the index you create in AI Foundry automatically selected.

    Select **Add to agent**

    ![Select AI Search index](./assets/7-select-ai-search-index.png)

1. Verify the knowledge source appears in your list.

1. TODO: Show the knowledge source working in the agent.

## 🧪 Lab 7.2: BYOM from Azure AI Foundry to your agent

In this lab, you'll put BYOM into practice by deploying a fine-tuned model that you will use in your agent.

### 7.2.2 Deploy a model

1. In the left-hand navigation, select **Fine-tuning**.

1. Select **+ Fine-tune model**. Search for `gpt-4.1-mini`.

    Select the `gpt-4.1-mini` model and select **Next**.
    ![Search model catalog](./assets/7-search-model-catalog.png)

1. You get a confirmation that a new Azure OpenAI resource will be created. 

    Select **Confirm**.

1. Now enter the details for your fine-tuned model:

    - **Connected AI resource**: This defaults to the OpenAI resource that was created for you
    - **Method**: Select `Supervised`
    - **Base model**: Select the `gpt-4.1-mini` model
    - **Training type**: Select `Standard`
    - **Automatically deploy when fine-tuning is complete**: Select `No`
    - **Deployment type**: Select `Developer`

    ![Create the fine-tuned model](./assets/7-create-fine-tuned-model.png)

1. Now it's time to add your training data.

    Select **+ Add training data**

    In the **Training data** dropdown, select **Upload files**

    Select **Upload file**

    Navigate to the folder containing the `hr_policy_training_data.jsonl` file. Select it and select **Open**.

    Select **Apply**

    ![Fine tune the model](./assets/7-fine-tune-the-model.png)

1. With your fine-tuned model details entered and your training data added, you're ready to create the model.

    Select **Submit**.

1. AI Foundry will queue the fine-tuning job, and it will take some time to fine-tune the model. When the process is complete, the status will change from **Queued** to **Completed**.

    ![Fine-tuned model](./assets/7-fine-tuning.png)

1. Now it's time to deploy the fine-tuned model. Select **Use this model**.

1. Enter `gpt-4.1-mini-fine-tuned` for the **Deployment name**

    Select **Deploy**

1. AI Foundry displays the details of your model deployment. Note the following information from the model deployment, as you'll need it later:

    - **Target URI**: This is the URL for our model's endpoint.
    - **API Key**: This is the primary key for authentication.
    - **Deployment name**: This is the name you chose (or left default) when deploying the model.

    ![Fine tuned model](./assets/7-model-deployment-details.png)

**Important:** Keep your API key secure. Don't share it or commit it to source control.

### 7.2.3 Use the model in a prompt

Now we will add the fine-tuned model to the Policy Assistant agent.

1. In the navigation bar, select **Tools**. Select **+ Add a tool**.

    Select **+ New tool**, and then select **Prompt**.

1. Enter `HR policy prompt` for the name

1. In the **Model** dropdown, select **+** next to **Azure AI Foundry Models**

1. Select **Connect a new model** and enter the details:

    - **Model deployment name**: Enter `gpt-4-1-mini-fine-tuned`
    - **Base model name**: Enter `gpt-4.1-mini`
    - **Azure model endpoint URL**: Enter the URI from your model details from Azure AI Foundry
    - **API Key**: Enter the API key from your model details in AI Foundry

    Select **Connect**

    ![Connect a model](./assets/7-connect-model.png)

1. In the **Instructions** for the prompt, enter this prompt:

```text
You are Contoso's HR Policy Assistant, a helpful and knowledgeable AI that answers employee questions about HR policies, benefits, and workplace guidelines.

   ## Your Role
   - Answer questions accurately based on Contoso's policies
   - Be friendly, professional, and concise
   - If you don't know something specific, be honest and direct them to HR
   - Use specific numbers, dates, and details when relevant

   ## Guidelines
   - Keep answers clear and easy to understand
   - Break down complex policies into simple terms
   - Include specific examples when helpful
   - Direct employees to appropriate resources or contacts when needed

   ## Employee Question
   

   ## Your Answer
   Provide a clear, accurate answer:
```

1. Under `Employee Question`, type `/` and select **Text**. Enter these details:

    - **Input**: `EmployeeQuestions`
    - **Sample data**: `What is the PTO policy?`

    Select **Close**

    Select **Save**

    ![Create prompt details](./assets/create-prompt-details.png)

1. Select **Add to agent**. The prompt is now ready to be used in your agent.

1. Test the prompt in the agent by asking a question like `What is the PTO policy?` and `What's the 401k match?`. The prompt will use the fine-tuned model to give specific answers.

    ![Testing the prompt](./assets/test-prompt.png)

## ✅ Mission Complete

Congratulations! 👏🏻 You've successfully extended your Copilot Studio agent with Azure AI capabilities using both BYOM and BYOD approaches.

You've learned how to:

- Deploy custom AI models in Azure AI Foundry
- Create custom prompt actions that leverage your deployed models
- Build searchable knowledge bases with Azure AI Search
- Connect enterprise data sources to your agent for grounded responses

These capabilities unlock powerful enterprise scenarios and allow you to create truly intelligent, context-aware agents that leverage your organization's data and specialized AI models.

## 📚 Tactical Resources

🔗 [Azure AI Foundry documentation](https://learn.microsoft.com/azure/ai-studio/?WT.mc_id=aiml-0000-cxa)

🔗 [Custom prompt actions in Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/advanced-generative-actions?WT.mc_id=power-0000-cxa)

🔗 [Azure AI Search documentation](https://learn.microsoft.com/azure/search/?WT.mc_id=aiml-0000-cxa)

🔗 [Knowledge sources in Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/knowledge-source-azure-ai-search?WT.mc_id=power-0000-cxa)

🔗 [Best practices for prompt engineering](https://learn.microsoft.com/azure/ai-services/openai/concepts/prompt-engineering?WT.mc_id=aiml-0000-cxa)

📺 [Bring Your Own AI Models to Copilot Studio](https://www.youtube.com/watch?v=example)

📺 [Grounding Copilot with Azure AI Search](https://www.youtube.com/watch?v=example)

```text
"How much PTO do I get after 5 years?"
"What's the 401k match?"
"Can I work remotely from Canada for 2 weeks?"
"What's covered by the home office stipend?"
"How many weeks of parental leave for non-birth parents?"
"What holidays does Contoso observe?"
"How do I request bereavement leave?"
"What's the tuition reimbursement limit?"
```
