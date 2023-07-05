# Net_Practice

This repository contains the solutions for the NetPractice Network Configuration Project. The project aims to develop a better understanding of TCP/IP addressing and network configuration by completing a series of exercises.

The project consists of 10 levels, each representing a non-functioning network diagram. The goal is to identify and resolve the issues to make the network run properly. A web-based training interface is provided to simulate the network configurations.

## How to use?

1. Download the project files from the attached file on the project's page.
2. Extract the files to a preferred folder on your local machine.
3. Open the folder and run the `index.html` file in a web browser. In training mode, you need to insert your username in the `Username` field and click `Start`.
> If the index.html don't work correctly in Firefox, I recommend using the Google Chrome browser.

## What to submit?
After performing each exercise a button called `get my config` appears. By clicking this button, a JSON file will be generated with your solution for the level. You should do this for each level and send the JSON files from the 10 levels in the Repository root folder.

## Useful Links
- [lpaube's Guide to NetPractice](https://github.com/lpaube/NetPractice)
- [Curso de Endereçamento IP](https://www.youtube.com/playlist?list=PLAp37wMSBouCU49LV0qFbItufigjYk-sp)
- [Network Fundamentals](https://www.youtube.com/playlist?list=PLDQaRcbiSnqF5U8ffMgZzS7fq1rHUI3Q8)

## My Solutions

<details>
  <summary>Level 1</summary>

##### Goals
- `🖥️ A` comunicate with `🖥️ B`
- `💻 C` comunicate with `🖥️ D`

#### Founded Issues
- [ ] - `🖥️ A` and `🖥️ B` has an established cable connection but they are using a different IP address range.
- [ ] - `💻 C` and `🖥️ D` has an established cable connection but they are using a different IP address range.

#### How to fix?
1. Change `📶 A1 IP address` to the same of `📶 B1` but change the last octet to the next number.
2. Change `📶 C1 IP address` to the same of `📶 D1` but change the last octet to the next number.

</details>

<details>
  <summary>Level 2</summary>

##### Goals
- `🖥 B` comunicate with `🖥 A`
- `🖥 D` comunicate with `🖥 C`

#### Founded Issues
- [ ] - `🖥 A` and `🖥 B` has an established cable connection and have a similar IP address but they have a different Mask.
- [ ] - `🖥 C` and `🖥 D` has an established cable connection and have a similar IP address but they are using a private IP address.

#### How to fix?
1. Change `📶 B1 Mask` to the same of `📶 A1`
2. Change `📶 A1 IP address` to the same of `📶 B1 IP address` but change the last octet to the previous number.
3. Change `📶 C1 IP address` to `192.168.1.253`
3. Change `📶 D1 IP address` to `192.168.1.254`

</details>

<details>
  <summary>Level 3</summary>

##### Goals
- `🖥 A` comunicate with `🖥 B`
- `🖥 A` comunicate with `🖥 C`
- `🖥 B` comunicate with `🖥 C`

#### Founded Issues
- [ ] - The 3 computers are connected to each other trought a switch but they are using different Masks and IP address ranges.

#### How to fix?
1. Change `📶 A1 Mask` to the same of `📶 C1`
2. Change `📶 B1 Mask` to the same of `📶 C1`
3. Change `📶 C1 IP address` to the same of `📶 A1` but change the last octet to the previous number.
4. Change `📶 B1 IP address` to the same of `📶 A1` but change the last octet to the next number.

</details>

<details>
  <summary>Level 4</summary>

##### Goals
- `🖥 A` comunicate with `🖥 B`
- `🖥 A` comunicate with `🔗 R`

#### Founded Issues
- [ ] `📶 R1, A1 and B1` masks are wrong when its compared with `📶 R2 and R3`
- [ ] `📶 R1 and B1` are using a different IP address range when its compared with `📶 A1`

#### How to fix?
1. Change `📶 R1 Mask` to the same of `📶 R2`
2. Change `📶 A1 Mask` to the same of `📶 R2`
3. Change `📶 B1 Mask` to the same of `📶 R2`
4. Change `📶 R1 IP address` to the same of `📶 A1` but change the last octet to the previous number.
5. Change `📶 B1 IP address` to the same of `📶 A1` but change the last octet to the next number.

</details>

<details>
  <summary>Level 5</summary>

##### Goals
- `🖥 A` comunicate with `🔗 R`
- `🖥 B` comunicate with `🔗 R`
- `🖥 A` comunicate with `🖥 B`

#### Founded Issues
- [ ] `🔄 A From and To` are wrong
- [ ] `📶 A1` has a mask and ip address different from `📶 R1`
- [ ] `🔄 B To` is wrong
- [ ] `📶 B1` has a mask and ip address different from `📶 R2`

#### How to fix?
1. Change `🔄 A From` to `default`
2. Change `🔄 A To` to `📶 R1 IP adress`
3. Change `📶 A1 Mask` to the same of `📶 R1`
4. Change `📶 A1 IP address` to the same of `📶 R1` but change the last octet to the previous number.
5. Change `🔄 B To` to `📶 R2 IP adress`
6. Change `📶 B1 Mask` to the same of `📶 R2`
7. Change `📶 B1 IP address` to the same of `📶 R2` but change the last octet to the previous number.

</details>

<details>
  <summary>Level 6</summary>

##### Goals
- `🖥 A` connect with the `🌐 Internet`

#### Founded Issues
- [ ] `📶 A1 and R1` are in the wrong range of Mask and IP address.
- [ ] `🔄 A To` don't points to the correct `📶 R1 IP address`.
- [ ] `🔄 R From` is wrong.
- [ ] `🔄 Internet From` don't points to `📶 A1 IP address`.

#### How to fix?
1. Change `📶 A1 Mask` to the same of `📶 R1 Mask`
2. Change `📶 R1 IP address` to the same of `📶 A1 IP address` but change the last octet to the previous number.
3. Change `🔄 A To` to `📶 R1 IP address`
4. Change `🔄 R From` to `default`
5. Change `🔄 Internet From` to `📶 A1 IP address` plus CIDR Notation of its Mask. In this case `34.146.38.227/25`

</details>

<details>
  <summary>Level 7</summary>

#### Goals
- `🖥 A` comunicate with `🖥 C`

#### Founded Issues
- [ ] `📶 A1 and R11` are in the wrong range because the others R's network are using next ranges.
- [ ] `🔄 A To` don't points to the correct `📶 R11 IP address`.
- [ ] `🔄 R1 To` is wrong.
- [ ] `📶 R12, R21, R22 and C1 Masks` are wrong
- [ ] `📶 R21, R22 and C1 IṔ address` are wrong
- [ ] `🔄 R2 To` is wrong.
- [ ] `🔄 C1 To` is wrong.

#### How to fix?
1. Change all Masks to '/26'
2. Change `🔄 A To` to `📶 R11 IP address`
3. Change `📶 R21 IP address` to the same of `📶 R11 IP address` but change the last octet to the previous number.
4. Change `🔄 R1 To` to `📶 R21 IP address`
5. Change `🔄 R2 To` to `📶 R12 IP address`
6. Change `📶 R22 IP address` to `103.198.14.65`
7. Change `📶 C1 IP address` to `103.198.14.66`
8. Change `🔄 C1 To` to `📶 R22 IP address`

</details>
