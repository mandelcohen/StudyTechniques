<h1 align="center">Tools for Effective Note-Taking</h1>
<br/><br/>

#### Table of contents:
- Markdown
- Mermaid
- Debugging
<br/><br/>

## MARKDOWN
This is a README file where you can use markdown to gather notes under headers and sub-headers, inserting `code snippets` and highlighting the information that stands out to you. It’s a the simple and easy-to-use markup language you can use to format virtually any document.
<br/><br/>

## Use markdown in a README on GitHub
*Example from 104-csharp-oop-basics, basically Marcs slides **but in your own words**:*
<br/><br/>
_______

### Fields in C#

- Fields are like variables, but they're tied to an instance of a class.

```cs
public class Assignment {
    public bool completed;
    public string description;
}
```

- To assign values to these fields, the class needs to be instantiated. This is where objects come into play.

```cs
Assignment playerGold = new();
playerGold.description = "Print the value of 200 gold to the console";
playerGold.completed = true;
```

- You can access a field using the **member access operator** `.` on the class instance (the object). For example: `playerGold.compleated`. In this case, the completed field belongs to the playerGold object.
<br/>

#### You can make tables to track your progress:
| OOP             | Assignments    | Status                |
|-----------------|----------------|-----------------------|
| Classes/Objects | P1_1 + Final   | DONE, need more notes |
| Fields          | P2_1-2 + Final | DONE                  |
| Methods         | P3_1-3 + Final | Awaiting feedback..   |
| Heap            | …              |                       |
| Inheritance     | …              |                       |
| Composition     | …              |                       |

#### or a task list:

- [x] Classes/Objects (Need notes)
- [x] Fields
- [ ] Methods 

##### to mention a few examples.
_______
<br/>

### The best part, fill your notes with hyperlinks:

All slides and assignments [here](https://github.com/marczaku/104-csharp-oop-basics/tree/main), check out this tutorial from W3 for further [reading](https://www.w3schools.com/cs/cs_oop.php) and there’s also the official language [documentation](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/) on Microsoft Learn. 

<br/><br/>

## Use markdown in an application
<br/>

- I use an app called [Bear](https://bear.app) where I use markdown to format my notes (only Mac). Equivalent options that works on all platforms are [UpNote](https://getupnote.com) or [Obsidian](https://obsidian.md).
<br/>

- Another option is [Notion](https://www.notion.so) which is more of a workspace, rather than stacking up notes you’re able to build your personal wiki and utilise a bunch of other functionalities like project planning.
<br/>

### A huge advantage of using an application for your notes is the **search functionality**:
<img width="1283" alt="searchInBear" src="https://github.com/user-attachments/assets/40f7902c-b58a-452b-bab2-9641567413d8">

<br/><br/>

## Use Markdown for descriptive READMEs for your projects:
<br/>

We are often asked to create descriptive READMEs with our game projects as part of our assignments, these are a great addition to include in our portfolios. Here are a few exaples from the [Pathfinding](https://github.com/forsbergsskola-se/gp23-Pathfinding-Mandel/blob/main/README.md) workshop, SDL [Space Invaders](https://github.com/forsbergsskola-se/gp23-203-opengl-game-magge/blob/main/README.md), and the [Unreal Game Project](https://github.com/mandelcohen/PURRPLEXED/blob/main/README.md).
<br/><br/>

## Resources on Markdown syntax

<br/>

- GitHub guide [here](https://gist.github.com/nikhilnayyar002/7a35e653d3d590e317c829243e73b110nikhilnayyar002/7a35e653d3d590e317c829243e73b110%29).
<br/>

- Open source MarkdownGuide [here](https://www.markdownguide.org/basic-syntax/).

_______
<br/>

## MERMAID

Mermaid Diagrams is a JavaScript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically. Mermaid syntax described [here](https://mermaid.js.org/intro/syntax-reference.html) and a very handy live editor [here](https://mermaid.live/).
<br/>

### Mindmaps:

An overview of the key subjects of the presentation:
```mermaid
mindmap
  root((MINDMAP))
    LEARNING
      Encoding<br/>Consolidation<br/>Retriveal
    TECHNIQUES
      Elaboration
        Use your<br/>own words
        Connect to<br/>previous knowledge
      Active Retriveal
        Most effective!
        Use in combination<br/>with other techniques
      Spaced Repitition
        The Forgetting Curve
      Chunking
        Break in to<br/>smaller parts
        Gain an overview
    TOOLS
      Memory techniques
      Effective<br/>note-taking
```

### Flowcharts

Here is an exapmle of a turn-based game loop, like in NIM or Tic-Tac-Toe:
```mermaid
flowchart TD
    Start([Start Game])
    PlayerTurn([Player's Turn])
    CheckWin{Check Win Condition}
    CheckDraw{Check Draw Condition}
    SwitchPlayer([Switch Player])
    EndGame([End Game])
    DeclareWinner([Declare Winner])
    DeclareDraw([Declare Draw])

    Start --> PlayerTurn
    PlayerTurn --> CheckWin
    CheckWin -- Yes --> DeclareWinner --> EndGame
    CheckWin -- No --> CheckDraw
    CheckDraw -- Yes --> DeclareDraw --> EndGame
    CheckDraw -- No --> SwitchPlayer
    SwitchPlayer --> PlayerTurn
```

### Sequence Diagram 

Shows the order of a sequence from top to bottom:
```mermaid
sequenceDiagram
    autonumber
    participant User
    participant LoginSystem
    User->>LoginSystem: Enter username and password
    alt Correct Credentials
        LoginSystem->>User: Login Success
    else Incorrect Credentials
        LoginSystem->>User: Login Failed
        loop Retry up to 3 times
            User->>LoginSystem: Re-enter credentials
        end
        LoginSystem->>User: Block after 3 failed attempts
    end
```

_______
<br/>

# DEBUGGING

I really can't stress this enough, the debugger is you're best friend during your learning process! Familiarise yourselfes with Rider's Debugging [tool](https://www.jetbrains.com/help/rider/Debugging_Code.html) and use it often when developing console applications, attach it to [Unity](https://www.jetbrains.com/guide/gamedev/tutorials/rider-for-unity/debugging/) to fix bugs, and to verify that your code does exactly what it's supposed to.

<br/>

_______
<br/>

