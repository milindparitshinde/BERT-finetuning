# BERT Finetuning

## Objective
Finetuning pre trained Google's BERT model on the desired context to get the required answers of the questions asked. It will be a QnA model returning the relevent text based on the question by preserving the core idea.

Bert model generates start and end index to get the relevent text from the context, for the question(s) asked.
**Example:**
consider -> _context = "The giraffe is a large African hoofed mammal belonging to the genus Giraffa. It is the tallest living terrestrial animal and the largest ruminant on Earth. Traditionally, giraffes were thought to be one species, Giraffa camelopardalis, with nine subspecies. Most recently, researchers proposed dividing them into up to eight extant species due to new research into their mitochondrial and nuclear DNA, as well as morphological measurements. Seven other extinct species of Giraffa are known from the fossil record."_

and _question = "How many Giraffes species are there?"_

model will generate start and end index to get the relevent text from the context for the question asked (In this example start and end index is 85 i.e. "eight").
<img width="1493" height="740" alt="Screenshot 2026-01-31 at 12 23 58 AM" src="https://github.com/user-attachments/assets/2d294444-1f18-452f-ba25-f876c79bfa2e" />


1.  Importing required libraries
<img width="330" height="189" alt="Screenshot 2026-01-30 at 11 59 01 PM" src="https://github.com/user-attachments/assets/4d4b9353-cd36-46af-818b-e840588b1a27" />

2.  model and token initialization.
<img width="1488" height="416" alt="Screenshot 2026-01-31 at 12 01 21 AM" src="https://github.com/user-attachments/assets/7efccc65-cbb7-4644-91ad-cb1369264414" />

3.  Defining a function that will take content and the question to provide the nessasary response.
<img width="1496" height="736" alt="Screenshot 2026-01-31 at 12 01 59 AM" src="https://github.com/user-attachments/assets/92d419c2-98b2-4661-922c-125d4693ebbe" />

### Limitation
One of it's limiations is it's squenence length which is 512, if length > 512 then it's truncated.
<img width="366" height="464" alt="Screenshot 2026-01-31 at 12 05 28 AM" src="https://github.com/user-attachments/assets/0c12001b-5b12-4c67-82e6-afe6acdaf826" />

<img width="1543" height="511" alt="Screenshot 2026-01-31 at 12 05 54 AM" src="https://github.com/user-attachments/assets/6b23dee0-5515-4258-b0d3-0ab8fc023c60" />

<img width="1399" height="339" alt="Screenshot 2026-01-31 at 12 06 31 AM" src="https://github.com/user-attachments/assets/dc9eca72-f0d0-4007-98cd-9a1ae87ad9fc" />

### Triumph
Divivde the sentence into chuncks to overcome this limitation

<img width="522" height="623" alt="Screenshot 2026-01-31 at 12 10 59 AM" src="https://github.com/user-attachments/assets/bea55467-7a7c-4971-a5cd-071d5af427d8" />

<img width="1231" height="635" alt="Screenshot 2026-01-31 at 12 11 28 AM" src="https://github.com/user-attachments/assets/28e7829b-bbba-49d2-8313-c523281cc3d4" />
