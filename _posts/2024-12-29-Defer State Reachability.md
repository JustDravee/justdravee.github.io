---
title: "Tip: Defer State Reachability"
date: 2024-12-29
categories: [creativity, speed_boost, finding_bugs]

---

The idea is in [this tweet](https://x.com/BowTiedDravee/status/1872741659164983656): 

<img width="645" alt="image" src="https://github.com/user-attachments/assets/b7893383-d22a-406b-8c12-b76deb273f2b" />

However, a tweet being short, it was a bit confusing:

<img width="613" alt="image" src="https://github.com/user-attachments/assets/97e66d44-84eb-49a0-a8dc-abce1fe2bdbd" />

So, a follow-up description was given: 

<img width="645" alt="image" src="https://github.com/user-attachments/assets/be0ea4db-3253-41d7-8a6a-697dc9f82775" />

Then, **an amazing description** came from [Antonio Viggiano](https://x.com/agfviggiano)'s ChatGPT prompt. I couldn't have explained this better. It did an amazing job understanding the insights I tried to fit in a tweet:

![image](https://github.com/user-attachments/assets/a3f373a2-0e2d-4a1b-b407-4d6edc16bd90)

![image](https://github.com/user-attachments/assets/1a0a14ce-df50-4b2b-aeb0-a21473cf216f)

![image](https://github.com/user-attachments/assets/19779fb9-4bf2-4177-b675-3af632331f68)

![image](https://github.com/user-attachments/assets/8125bbf8-9762-45c5-b298-5a7db1c71fd6)

To me, this tip actually belongs to the "creativity" category as getting assumptions on reads is quite easy (and will close your mind). This here will keep you looking for bad paths without assuming that they "can't be reached". Also, if they can't be reached for now, a future code change could make it happen, therefore you could still submit a suggestion in how to harden the code. 

The speed boost is thanks to the better direction of effort.


