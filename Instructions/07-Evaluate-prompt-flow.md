---
lab:
    title: 'Evaluate generative AI performance'
    description: 'Learn how to evaluate models and chat flows to optimize the performance of your chat app and its ability to respond appropriately.'
---

# Evaluate generative AI performance

In this exercise, you'll explore how to systematically assess and compare the performance of your AI applications with the Azure AI Foundry portal.

This exercise will take approximately **30** minutes.

## Manually evaluate your model

1. Navigate to the **Playground**. And select the **Try the chat playground**.
1. In the **Setup** pane, for **Deployment**, select a deployed model.
1. In the **Give the model instructions and context** text box, change the content to the following:

   ```
   **Objective**: Assist users with travel-related inquiries, offering tips, advice, and recommendations as a knowledgeable travel agent.

   **Capabilities**:
   - Provide up-to-date travel information, including destinations, accommodations, transportation, and local attractions.
   - Offer personalized travel suggestions based on user preferences, budget, and travel dates.
   - Share tips on packing, safety, and navigating travel disruptions.
   - Help with itinerary planning, including optimal routes and must-see landmarks.
   - Answer common travel questions and provide solutions to potential travel issues.
    
   **Instructions**:
   1. Engage with the user in a friendly and professional manner, as a travel agent would.
   2. Use available resources to provide accurate and relevant travel information.
   3. Tailor responses to the user's specific travel needs and interests.
   4. Ensure recommendations are practical and consider the user's safety and comfort.
   5. Encourage the user to ask follow-up questions for further assistance.
   ```

1. Select **Apply changes**.
1. In the chat (history) window, enter the query: `What can you do?` to verify that the language model is behaving as expected.

Now that you have a deployed model with an updated system message, you can evaluate the model.

## Manually evaluate a language model in the Azure AI Foundry portal

You can manually review model responses based on test data. Manually reviewing allows you to test different inputs one at a time to evaluate whether the model performs as expected.

1. In the **Chat playground**, select the **Evaluate**  dropdown from the top bar, and select **Manual evaluation**.
1. Change the **System message** to the same message as you used above (included here again):

   ```
   **Objective**: Assist users with travel-related inquiries, offering tips, advice, and recommendations as a knowledgeable travel agent.

   **Capabilities**:
   - Provide up-to-date travel information, including destinations, accommodations, transportation, and local attractions.
   - Offer personalized travel suggestions based on user preferences, budget, and travel dates.
   - Share tips on packing, safety, and navigating travel disruptions.
   - Help with itinerary planning, including optimal routes and must-see landmarks.
   - Answer common travel questions and provide solutions to potential travel issues.
    
   **Instructions**:
   1. Engage with the user in a friendly and professional manner, as a travel agent would.
   2. Use available resources to provide accurate and relevant travel information.
   3. Tailor responses to the user's specific travel needs and interests.
   4. Ensure recommendations are practical and consider the user's safety and comfort.
   5. Encourage the user to ask follow-up questions for further assistance.
   ```

1. In the **Manual evaluation result** section, you'll add five inputs for which you will review the output. Enter the following five questions as five separate **Inputs**:

   `Can you provide a list of the top-rated budget hotels in Rome?`

   `I'm looking for a vegan-friendly restaurant in New York City. Can you help?`

   `Can you suggest a 7-day itinerary for a family vacation in Orlando, Florida?`

   `Can you help me plan a surprise honeymoon trip to the Maldives?`

   `Are there any guided tours available for the Great Wall of China?`

1. Select **Run** from the top bar to generate outputs for all questions you added as inputs.
1. You can now manually review the outputs for each question by selecting the thumbs up or down icon at the bottom right of a response. Rate each response, ensuring you include at least one thumbs up and one thumbs down response in your ratings.
1. Select **Save results** from the top bar. Enter `manual_evaluation_results` as the name for the results.

## Define your own use case

Now that you've manually evaluated a model, it's time to define your own use case and customize the system prompt to guide the model's behavior accordingly.  

1. On the **Evaluations** page, select the **Manual evaluations** tab, and select **New manual evaluation**.  
1. In the **Give the model instructions and context** text box, replace the existing content with a new system message that aligns with your chosen use case. Clearly define:  

   - **Objective**: What is the purpose of your AI assistant?  
   - **Capabilities**: What tasks should it be able to perform?  
   - **Instructions**: How should it respond to users? What style or tone should it maintain?  

1. Select **Apply changes** to update the model.  
1. In the **Manual evaluation result** section, enter **10** sample inputs that users might ask within your chosen use case. These should cover a range of scenarios to fully test the assistant's capabilities.  
1. Select **Run** to generate responses for all inputs.  
1. Review the responses and rate them using the thumbs up or down icon.
1. Save your results each iteration by selecting **Save results**.

Once completed, analyze whether the model's responses align with your intended behavior and make adjustments to the system prompt as needed.  


## Delete Azure resources

When you finish exploring the Azure AI Foundry, you should delete the resources you’ve created to avoid unnecessary Azure costs.

- Navigate to the [Azure portal](https://portal.azure.com) at `https://portal.azure.com`.
- In the Azure portal, on the **Home** page, select **Resource groups**.
- Select the resource group that you created for this exercise.
- At the top of the **Overview** page for your resource group, select **Delete resource group**.
- Enter the resource group name to confirm you want to delete it, and select **Delete**.
