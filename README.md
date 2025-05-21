# Fine-Tuned Philosophy Chatbot

As part of my Big Data Systems class, I developed a chatbot fine-tuned on a dataset of philosophical dialogues. I used the **Hugging Face `philosophy_dialogue` dataset** (sourced from Hypersniper).

## 🧠 Dataset Integration & Model Fine-Tuning

To integrate the dataset, I modified the `tokenize_function` inside `prepare_dataset()` to accommodate the structure of the `philosophy_dialogue` data. This involved changing the input field from `'input'` to `'instruction'` to match the dataset’s formatting.

With these adjustments, I successfully fine-tuned the model using the entire dataset. The total training time was **55 minutes**. Below is a sample prompt and the corresponding model output:

**Prompt:**  
> What is the meaning of life?

**Generated Response:**  
> Life is not a simple question. It is an exploration of our lives, our emotions, our relationships, our relationships with others, and our understanding of ourselves. It is a journey that we must all share, not just for ourselves, but for all of us.  
>  
> But it is not the only life. It is also a journey that we must all strive for, for we must strive for our own happiness, for we must strive for our own fulfillment.

I was satisfied with the model’s philosophical tone and proceeded to deploy it with a Dockerized chatbot interface.

## 🧱 Deployment & Design

To make the experience immersive, I designed an interface inspired by **Socratic philosophy**:

- The UI features **white classical styling** reminiscent of ancient Greek marble and parchment.
- A header displays one of my favorite Socrates quotes to encourage introspective, meaningful questions.
- I added a custom **output-length control function** to manage how long the chatbot’s responses could be.

🎥 **Video Demo:**  
[Watch the chatbot in action](https://drive.google.com/file/d/1WvUIk3f656dnnYJAz5T17WWVX7xJCQyK/view?usp=sharing)
