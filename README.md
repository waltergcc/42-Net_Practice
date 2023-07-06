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
- [TCP/IP Model Explained](https://www.youtube.com/watch?v=OTwp3xtd4dg)

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
1. Change `📶 A1 IP address` to the same of `📶 B1` + 1.
2. Change `📶 C1 IP address` to the same of `📶 D1` + 1.

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
2. Change `📶 A1 IP address` to the same of `📶 B1 IP address` - 1.
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
3. Change `📶 C1 IP address` to the same of `📶 A1` - 1.
4. Change `📶 B1 IP address` to the same of `📶 A1` + 1.

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
4. Change `📶 R1 IP address` to the same of `📶 A1` - 1.
5. Change `📶 B1 IP address` to the same of `📶 A1` + 1.

</details>

<details>
  <summary>Level 5</summary>

##### Goals
- `🖥 A` comunicate with `🔗 R`
- `🖥 B` comunicate with `🔗 R`
- `🖥 A` comunicate with `🖥 B`

#### Founded Issues
- [ ] `🔄 A Dest and Jump_to` are wrong
- [ ] `📶 A1` has a mask and ip address different from `📶 R1`
- [ ] `🔄 B Jump_to` is wrong
- [ ] `📶 B1` has a mask and ip address different from `📶 R2`

#### How to fix?
1. Change `🔄 A Dest` to `default`
2. Change `🔄 A Jump_to` to `📶 R1 IP adress`
3. Change `📶 A1 Mask` to the same of `📶 R1`
4. Change `📶 A1 IP address` to the same of `📶 R1` - 1.
5. Change `🔄 B Jump_to` to `📶 R2 IP adress`
6. Change `📶 B1 Mask` to the same of `📶 R2`
7. Change `📶 B1 IP address` to the same of `📶 R2` - 1.

</details>

<details>
  <summary>Level 6</summary>

##### Goals
- `🖥 A` connect with the `🌐 Internet`

#### Founded Issues
- [ ] `📶 A1 and R1` are in the wrong range of Mask and IP address.
- [ ] `🔄 A Jump_to` don't points to the correct `📶 R1 IP address`.
- [ ] `🔄 R Dest` is wrong.
- [ ] `🔄 Internet Dest` don't points to `📶 A1 IP address`.

#### How to fix?
1. Change `📶 A1 Mask` to the same of `📶 R1 Mask`
2. Change `📶 R1 IP address` to the same of `📶 A1 IP address` - 1.
3. Change `🔄 A Jump_to` to `📶 R1 IP address`
4. Change `🔄 R Dest` to `default`
5. Change `🔄 Internet Dest` to `📶 A1 IP address` + CIDR Notation of its Mask. In this case `34.146.38.227/25`

</details>

<details>
  <summary>Level 7</summary>

#### Goals
- `🖥 A` comunicate with `🖥 C`

#### Founded Issues
- [ ] `📶 A1 and R11` are in the wrong range because the others R's network are using next ranges.
- [ ] `🔄 A Jump_to` don't points to the correct `📶 R11 IP address`.
- [ ] `🔄 R1 Jump_to` is wrong.
- [ ] `📶 R12, R21, R22 and C1 Masks` are wrong
- [ ] `📶 R21, R22 and C1 IṔ address` are wrong
- [ ] `🔄 R2 Jump_to` is wrong.
- [ ] `🔄 C1 Jump_to` is wrong.

#### How to fix?
1. Change all Masks to '/26'
2. Change `🔄 A Jump_to` to `📶 R11 IP address`
3. Change `📶 R21 IP address` to the same of `📶 R11 IP address` - 1.
4. Change `🔄 R1 Jump_to` to `📶 R21 IP address`
5. Change `🔄 R2 Jump_to` to `📶 R12 IP address`
6. Change `📶 R22 IP address` to `103.198.14.65`
7. Change `📶 C1 IP address` to `103.198.14.66`
8. Change `🔄 C1 Jump_to` to `📶 R22 IP address`

</details>

<details>
  <summary>Level 8</summary>

#### Goals
- `🖥 C` comunicate with `🖥 D`
- `🖥 C` connect with the `🌐 Internet`
- `🖥 D` connect with the `🌐 Internet`

#### Founded Issues
- [ ] `🔄 R1 and R2 Dest` are wrong.
- [ ] `🔄 All Dest except R2 are wrong.
- [ ] `📶 All masks except R12` are wrong.
- [ ] `📶 All IP address except R12` are wrong.

#### How to fix?
1. Change `🔄 Internet to` to `📶 R12 IP address`
2. Change `🔄 R1 and R2 Dest` to `default`
3. Change `📶 All Masks` to the same of `📶 R12 Mask`
4. Change `📶 R13 IP address` to the same of `🔄 R2 Jump_to`
5. Change `📶 R21 IP address` to the same of `📶 R13` - 1.
6. Change `🔄 R1 Jump_to` to `📶 R21`.
7. Change `📶 R23 IP address` to the same of `🔄 Internet Jump_to` + 1.
8. Change `📶 R22 IP address` to the same of `🔄 Internet Jump_to` + 17.
9. Change `📶 D1 IP address` to the same of `📶 R23` + 1.
10. Change `🔄 D Jump_to` to `📶 R23`.
11. Change `📶 C1 IP address` to the same of `📶 R22` + 1.
12. Change `🔄 C Jump_to` to `📶 R22`.

</details>

<details>
  <summary>Level 9</summary>

#### Goals
- `🖥 A` comunicate with `🖥 B`
- `🖥 C` comunicate with `🖥 D`
- `🖥 A` connect with the `🌐 Internet`
- `🖥 A` comunicate with `🖥 D`
- `🖥 B` comunicate with `🖥 C`
- `🖥 C` connect with the `🌐 Internet`

#### Founded Issues
- [ ] `🔄 Internet Dest` has many entries
- [ ] `🔄 R1 Jump_to` has many entries
- [ ] `📶 R11, R22 and R23 Subnets` are all wrong
- [ ] `📶 R12 and R13 IP address` are wrong

#### How to fix?
1. Delete 1 entry of `🔄 Internet Dest`
2. Delete 1 entry of `🔄 R1`
3. Change `🔄 Àll Jump_to` to `default`
4. Change `📶 R11 Subnet Mask` to the same of `📶 R11`
5. Change `📶 R11 IP address` to `42.5.4.1`
6. Change `🔄 A and B` to `📶 R11`
7. Change `📶 A1 IP address` to the same of `📶 R11` + 1
8. Change `📶 B1 IP address` to the same of `📶 R11` + 2
9. Change `🔄 Internet Dest` to 4`2.5.4.0/24`
10. Change `📶 R22 IP address` to `76.2.3.1`
11. Change `🔄 C Jump_to` to `76.2.3.1`
12. Change `📶 C1 IP address` to the same of `📶 R23` + 1
13. Change `🔄 Internet second Dest` to `76.2.3.0/24`
14. Change `📶 R23 IP address` to the same of `🔄 D Jump_to`
15. Change `📶 D1 Mask` to the same of `📶 R23`
16. Change `📶 D1 IP address` to the same of `📶 R23` + 1
17. Change `📶 R13 Mask` to the same of `📶 R21`
18. Change `📶 R21 IP address` to the same of `📶 R13` - 1
19. Change `🔄 R1 Jump_to` to `📶 R21`
19. Change `🔄 R2 Jump_to` to `📶 R13`

</details>

<details>
  <summary>Level 10</summary>

#### Goals
- `🖥 H1` comunicate with `🖥 H2`
- `🖥 H3` comunicate with `🖥 H4`
- `🖥 H1` connect with the `🌐 Internet`
- `🖥 H1` comunicate with `🖥 H4`
- `🖥 H2` comunicate with `🖥 H3`
- `🖥 H3` connect with the `🌐 Internet`
- `🖥 H4` connect with the `🌐 Internet`

#### Founded Issues
- [ ] `🔄 Internet Dest` not fill all IPs
- [ ] `🔄 R1 first Dest` is wrong
- [ ] `📶 H1 and H2 Masks` are wrong
- [ ] `📶 H2 IP address` is wrong
- [ ] `📶 R13 Mask` is wrong
- [ ] `📶 R22, R23 and H31 Mask and IP` are wrong
- [ ] `🔄 H3 Jump_to` is wrong

#### How to fix?
1. Change `🔄 Internet Dest` to `📶 R11 IP address` but with the last octet as `0` + CDIR notation /24
2. Change `📶 H1 and H2 Mask` to the same of `📶 R11`
3. Change `📶 H2 IP address` to the same of `📶 H1` + 1
4. Change `📶 R13 Mask` to the same of `📶 R12`
5. Change `📶 R23 Mask` to the same of `📶 H41`
6. Change `📶 R23 IP address` to the same of `🔄 H4 Jump_to`
7. Change `📶 R22 and H31 Mask` to `255.255.255.224`
8. Change `📶 R22 IP address` to `135.185.182.193`
9. Change `📶 H31 IP address` to the same of `R22` + 1
10. Change `🔄 H3 Jump_to` to `📶 R22`

</details>

## Grade: 100/100