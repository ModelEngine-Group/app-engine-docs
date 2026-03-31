---
layout: default
title: Configuring a Model
parent: Model Access
nav_order: 1
---

# Getting Started: Configuring Your Foundation Model Service

Welcome to **Model Configuration Application**. This application helps you quickly add models, set the default model, and bind API keys. It is applicable to service scenarios where multiple foundation models need to be integrated.

## Application Principle

This application encapsulates the following key capabilities through visualized workflows:

- Add custom model information (model name, baseUrl, and API key).
- Set the default model for subsequent chat to call.
- Delete models and exit model management.
- Automatically synchronize all configurations for the use by the platform or callers.

You only need to answer a few simple questions and the system will automatically complete the model configuration process.

## Procedure

### Step 1: View model configurations.

In **Application Market**, search for **Model Configuration Application**. Click **Start Configuration** in **Inspirations**, or directly initiate a chat.

### Step 2: Add a model.

Click **Add Model** and enter basic model information.

- **Model Name:** Enter a simple and recognizable name, for example, Qwen-7B-Chat.
- **Base URL:** API address of the model.
- **API Key:** key for invoking the model.

After the setting is complete, click **Confirm** to save the model to the system.

### (Optional) Step 3: Set the default model.

In the model list, click the operation menu of the target model and select **Set as Default Model**. The system will preferentially use the model for dialog and reasoning tasks.

### Step 4: Delete a model.

In the model list, click the operation menu of the target model and choose **Delete Model**. The system deletes the target model.
