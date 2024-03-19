# GPTAutoTrainer
Uses GPT 3.5 and 4 to Auto Tune GPT 3.5

GPT Auto Trainer is a Python script that automatically fine-tunes a base language model using the OpenAI API by leveraging the interaction between GPT-3.5 and GPT-4 models. The script takes a series of prompts as input, generates responses from both GPT-3.5 and GPT-4 models for each prompt, and then fine-tunes the base model using the generated responses as training data.

## ⚠️ Important Note: API Usage and Costs ⚠️

Please be aware that running the GPT Auto Trainer script will incur costs due to the usage of the OpenAI API. The script makes API calls to generate responses from GPT-3.5 and GPT-4 models and to fine-tune the base model. The exact cost will depend on the number of prompts, the size of the generated responses, and the fine-tuning parameters.

Make sure to review the OpenAI pricing details and monitor your API usage to avoid unexpected charges. It is highly recommended to set up billing alerts and usage limits in your OpenAI account to control costs.

## Prerequisites

Before running the GPT Auto Trainer script, ensure that you have the following:

- Python 3.6 or above installed
- OpenAI Python library installed (`pip install openai`)
- OpenAI API key obtained from the OpenAI website

## Setup

1. Clone the repository or download the script file.

2. Install the required dependencies by running the following command:
   ```
   pip install openai
   ```

3. Set the `OPENAI_API_KEY` environment variable with your OpenAI API key. You can do this by running the following command in your terminal or adding it to your system's environment variables:
   ```
   export OPENAI_API_KEY="your_api_key_here"
   ```

## Usage

1. Open the script file and modify the `prompts` list with your desired prompts for fine-tuning.

2. Adjust the `base_model` variable to specify the base model you want to fine-tune (e.g., "text-davinci-002").

3. Optionally, you can modify the fine-tuning parameters such as `n_epochs`, `batch_size`, and `learning_rate_multiplier` in the `auto_trainer` function to suit your requirements.

4. Run the script using the following command:
   ```
   python gpt_auto_trainer.py
   ```

5. The script will generate responses from GPT-3.5 and GPT-4 models for each prompt, create a training data file in JSONL format, and initiate the fine-tuning process using the OpenAI API.

6. Once the fine-tuning process is complete, the script will display the details of the fine-tuned model.

## Logging

The script includes logging functionality to provide information about the execution flow and any errors that occur. Log messages are displayed in the console and can be useful for monitoring and debugging purposes.

## Error Handling

The script incorporates error handling to catch and handle exceptions that may occur during API requests or the fine-tuning process. If an error occurs, an appropriate error message is logged, and the script continues execution.

## License

This project is licensed under the [MIT License](LICENSE).

## Disclaimer

GPT Auto Trainer is an experimental script and is provided as-is without any warranty. The authors and contributors of this script are not responsible for any costs, damages, or issues arising from the usage of this script or the OpenAI API. Use it at your own risk and discretion.
