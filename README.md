# Password-Generator-project

```python
import random
def create_password(length):
    letters = "abcdefghijklmnopqrstuvwxyz"
    caps = letters.upper()
    nums = "0123456789"
    symbols = "@#$&*!?"
    
    if length < 4:
        return "Length must be at least 4 to include all character types."

    mix = list(letters + caps + nums + symbols)

    # Ensure all character types are included
    result = [
        random.choice(letters),
        random.choice(caps),
        random.choice(nums),
        random.choice(symbols)
    ]

    while len(result) < length:
        result.append(random.choice(mix))

    random.shuffle(result)
    return "".join(result)

try:
    user_input = int(input("How long should the password be? "))
    final_password = create_password(user_input)
    print("\n Your new password:", final_password)
except:
    print("Please enter a valid number.")
```



<img width="1129" height="745" alt="image" src="https://github.com/user-attachments/assets/ac7fbdde-540a-4a49-b43f-4257f134cb1a" />


