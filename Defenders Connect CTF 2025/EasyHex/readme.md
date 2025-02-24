
![|375](https://i.imgur.com/WGBlEtJ.png)

**Points:** 100

**Challenge Description:**

Our admin, a whisper in the digital wind, Concealed their missives, lest secrets unpinned. To the project lead, words traveled veiled and sly, A method employed, where lightness kissed the sky.

"My code," they'd jest, "a feather's gentle grace, Yet holds a truth within its airy space." A string of symbols, intercepted with care, A jumble of characters, beyond compare.

Can you unravel the admin's cryptic art?

String: "`43 54 46 7b 48 45 58 5f 49 53 66 75 4e 7d`"

Challange created by Kushagra Varshney of Club Cyberonites

**Flag Format: CTF{a-zA-Z0-9_}**

---

**Question Analysis, Background and Solution**:

The challenge name “EasyHex” hints that it might involves hexadecimal values.

Let’s quickly brush up on what hex is and how to identify it.

**Hexadecimal Basics:**

Hexadecimal is a number system combining "hexa" for 6 and "deci" for 10. It uses 16 digits: 0 to 9 and A to F, where A stands for 10, B for 11, and so on. Each digit’s position has a weight 16 times greater than the previous one.

When converting to another system, multiply each digit by 16 raised to the power of its position. For example, in `7B3`:

- `7` is multiplied by (16^2)
- `B` (11 in decimal) by (16^1)
- `3` by (16^0)

https://www.geeksforgeeks.org/hexadecimal-number-system/
https://www.ascii-code.com/

Examples:

1. Hexadecimal Value: `43`
	1. Convert to Decimal:
	    - `4` in the 16’s place: (4 \times 16 = 64)
	    - `3` in the 1’s place: (3 \times 1 = 3)
	    - Add them together: (64 + 3 = 67)
	2. ASCII Table: The decimal value `67` corresponds to the character `C`.
	So, `43` in hexadecimal is `67` in decimal, which is the character `C` in the ASCII table.


Let’s take the hexadecimal value `4E` and convert it to its corresponding ASCII character.

1. Hexadecimal Value: `4E`
	1. Convert to Decimal:
	    - `4` in the 16’s place: (4 \times 16 = 64)
	    - `E` in the 1’s place: `E` is 14 in decimal, so (14 \times 1 = 14)
	    - Add them together: (64 + 14 = 78)
	2. ASCII Table: The decimal value `78` corresponds to the character `N`.
	So, `4E` in hexadecimal is `78` in decimal, which is the character `N` in the ASCII table.

We can also quickly check the ASCII table to convert hexadecimal values to characters.

![](https://i.imgur.com/51aqvvz.png)


Now let's back to the challenge:

So in the challenge an admin hid messages to the project lead using clever, cryptic methods. The intercepted symbols held hidden truths within their simple structure.

String -  `43 54 46 7b 48 45 58 5f 49 53 66 75 4e 7d`

We can see that the string contains characters in the range of 0 to 9 and A to F, indicating hexadecimal values.

We can convert these manually by referring to the ASCII table, or more conveniently, we can use CyberChef.

**CyberChef** is a web app designed for performing various “cyber” operations like encoding, encryption, and data analysis within a browser. It’s often called the “Cyber Swiss Army Knife.

To decode the string, we search for the term “hex” in CyberChef. We have “From Hex” and “To Hex” operations. This means if we want to encode a value into hex, we use “To Hex,” and if we want to decode from hex, we use “From Hex.”

![](https://i.imgur.com/EKtae8f.png)

Since we have to decode, we use “From Hex.” We will drag and drop the operation, and we can see from the screenshot below that we get the flag.

![](https://i.imgur.com/Urf1odU.png)

**Link to Solution** - https://cyberchef.org/#recipe=From_Hex('Auto')&input=NDMgNTQgNDYgN2IgNDggNDUgNTggNWYgNDkgNTMgNjYgNzUgNGUgN2Q

**Flag** : CTF{HEX_ISfuN}
