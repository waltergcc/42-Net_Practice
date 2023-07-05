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

### Level 1

##### Goals
- `🖥️A` comunicate with `🖥️B`
- `💻C` comunicate with `🖥️D`

#### Founded Issues
- [ ] - `🖥️A` and `🖥️B` has an established cable connection but they are using a different IP address range.
- [ ] - `💻C` and `🖥️D` has an established cable connection but they are using a different IP address range.

#### How to fix?
1. Change `📶A1 IP address` to the same of `📶B1` but change the last octet to the next number.
2. Change `📶C1 IP address` to the same of `📶D1` but change the last octet to the next number.

### Level 2

##### Goals
- `🖥B` comunicate with `🖥A`
- `🖥D` comunicate with `🖥C`

#### Founded Issues
- [ ] - `🖥A` and `🖥B` has an established cable connection and have a similar IP address but they have a different Mask.
- [ ] - `🖥C` and `🖥D` has an established cable connection and have a similar IP address but they are using a private IP address.

#### How to fix?
1. Change `📶B1 Mask` to the same of `📶A1`
2. Change `📶A1 IP address` to the same of `📶B1 IP address` but change the last octet to the previous number.
3. Change `📶C1 IP address` to `192.168.1.253`
3. Change `📶D1 IP address` to `192.168.1.254`

