%title: Command Line Curiosities
%author: Hamza Haiken (@2xhTenchi)
%date: XXXX-XX-XX















-> # Command Line Curiosities

-> Python Utrecht Meetup
-> January 2018

---












-> ──────────────────────┤ Contents ├──────────────────────


-> 1. _Introduction_ . . . . . . . . . . . .  Who? What? Why?

-> 2. _Tools of the trade_ . . . . . . . . What you will need

-> 3. _Delving deeper_ . . . . . . . .  Techniques & Showcase


-> ────────────────────────────────────────────────────────

---

-> # 1. Introduction











-> ┌───────────────────────────────────┐
-> │ *root:~/slides$* whoami             │
-> │ root                              │
-> │                                   │
-> │ *root:~/slides$* \_                  │
-> │                                   │
-> │                                   │
-> │                                   │
-> └───────────────────────────────────┘

---

# 1. Introduction

## 1.1 Who?

->  ═════╦═════ 
->  ╔═══╦╩╦═══╗ 
->  ╚═╗ ║ ║ ╔═╝ 
->  ║ ║ ║ ║ ║ ║ 
->  ╚═══╝ ╚═══╝ 
-> ╔═╬═╗  ═╗ ╔═ 
-> ║ ║ ║ ╔═╬═╬═╗
-> ║ ║ ║ ║ ║ ║ ║
-> ║ ║ ║ ╚═╣ ╠═╝
-> ══╩══   ╚═╩═ 

^
-> Hamza "Tenchi" Haiken
-> 天  地   

^
-> @2xhTenchi 
^
-> http://tenchi.me 

^
-> *CODE.STΛR* for > 2 years

^
-> Writes at least 1 line of Python a day

^
-> _Really_ likes terminals 

---

# 1. Introduction



## 1.2 What?

- Graphical *experiments* in the terminal

- Hobby projects

- Open source: *http://github.com/Tenchi2xh*



## 1.3 Why?

- Do something different

- Push the limits

- Have fun

^
-> *╔═════════════════════════════╗*
-> *║*  LIVE DEMO: Existing stuff  *║*
-> *╚═════════════════════════════╝*

---

-> # 2. Tools of the trade









->                                \_   \_    
->                               ( \\\_/ )   
->                  \_   \_       \_\_) \_ (\_\_  
->          \_   \_  ( \\\_/ )  \_  (\_\_ (\_) \_\_) 
->         ( \\\_/ )\_\_) \_ (\_\_( \\\_/ )) \_ (    
->        \_\_) \_ ((\_\_ (\_) \_\_)) \_ ((\_/ \\\_)   
->       (\_\_ (\_) \_\_)) \_ ((\_\_ (\_) \_\_)       
->          ) \_ (  (\_/ \\\_)  ) \_ (          
->         (\_/ \\\_)         (\_/ \\\_)         

---

# 2. Tools of the trade

## 2.1 ASCII





- 7-bit ASCII, 128 chars

- 8-bit ASCII, 256 chars (Extended ASCII)

^
  - PETSCII

  - *Code page 437*

^
  - Mac OS Roman

^
  - ISO/IEC 8859


---

# 2. Tools of the trade

## 2.1 ASCII

-> Extended ASCII: code page 437

^
->        0x\_0 0x\_1 0x\_2 0x\_3 0x\_4 0x\_5 0x\_6 0x\_7 0x\_8 0x\_9 0x\_a 0x\_b 0x\_c 0x\_d 0x\_e 0x\_f
->      ┌────────────────────────────────────────────────────────────────────────────────
-> 0x0\_ │ NULL SOH  STX  ETX  EOT  ENQ  ACK  BEL  BS   HT   LF   VT   FF   CR   SO   SI  
-> 0x1\_ │ DLE  DC1  DC2  DC3  DC4  NAK  SYN  ETB  CAN  EM   SUB  ESC  FS   GS   RS   US  
^
-> 0x2\_ │      \!    "    #    $    %    &    '    (    )    \*    +    ,    -    .    /   
-> 0x3\_ │ 0    1    2    3    4    5    6    7    8    9    :    ;    <    =    >    ?   
^
-> 0x4\_ │ @    A    B    C    D    E    F    G    H    I    J    K    L    M    N    O   
-> 0x5\_ │ P    Q    R    S    T    U    V    W    X    Y    Z    [    \\    ]    ^    \_   
-> 0x6\_ │ \`    a    b    c    d    e    f    g    h    i    j    k    l    m    n    o   
-> 0x7\_ │ p    q    r    s    t    u    v    w    x    y    z    {    |    }    ~    DEL 
^
->      ├──────────────────────────────────────────────────────────────────────────────── 
-> 0x8\_ │ Ç    ü    é    â    ä    à    å    ç    ê    ë    è    ï    î    ì    Ä    Å   
-> 0x9\_ │ É    æ    Æ    ô    ö    ò    û    ù    ÿ    Ö    Ü    ¢    £    ¥    ₧    ƒ   
-> 0xa\_ │ á    í    ó    ú    ñ    Ñ    ª    º    ¿    ⌐    ¬    ½    ¼    ¡    «    »   
^
-> 0xb\_ │ *░    ▒    ▓    │    ┤    ╡    ╢    ╖    ╕    ╣    ║    ╗    ╝    ╜    ╛    ┐*   
-> 0xc\_ │ *└    ┴    ┬    ├    ─    ┼    ╞    ╟    ╚    ╔    ╩    ╦    ╠    ═    ╬    ╧*   
-> 0xd\_ │ *╨    ╤    ╥    ╙    ╘    ╒    ╓    ╫    ╪    ┘    ┌    █    ▄    ▌    ▐    ▀*   
^
-> 0xe\_ │ α    ß    Γ    π    Σ    σ    µ    τ    Φ    Θ    Ω    δ    ∞    φ    ε    ∩   
-> 0xf\_ │ ≡    ±    ≥    ≤    ⌠    ⌡    ÷    ≈    °    ∙    ·    √    ⁿ    ²    ■    NBSP



---

# 2. Tools of the trade

## 2.1 ASCII




^
-> ┌─────┬─┐  ╔═════╦═╗  ╓─────╥─╖  ╒═════╤═╕
-> │     │ │  ║     ║ ║  ║     ║ ║  │     │ │
-> │     │ │  ║     ║ ║  ║     ║ ║  │     │ │
-> ├─────┼─┤  ╠═════╬═╣  ╟─────╫─╢  ╞═════╪═╡
-> └─────┴─┘  ╚═════╩═╝  ╙─────╨─╜  ╘═════╧═╛




^
->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████
->  ░ ░ ░░░░▒░▒░▒▒▒▒▓▒▓▒▓▓▓▓█▓█▓██████
->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████
->  ░ ░ ░░░░▒░▒░▒▒▒▒▓▒▓▒▓▓▓▓█▓█▓██████
->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████

---

# 2. Tools of the trade

## 2.1 ASCII

-> Microsoft MS-DOS 6.22 Setup                                                   
-> ═══════════════════════════                                                   
->                                                                               
->          Increase your hard disk space with DriveSpace. MS-DOS 6.22           
->          gives you a safe, easy way to increase disk capacity by              
->          integrating data compression into the operating system.              
->                                                                               
->          If yo `┌──────────────────────────────────────────────┐`               
->          incre `│                                              │`               
->          promp `│ Please insert the following disk in drive A: │`               
->                `│                                              │`               
->                `│                 Setup Disk #2                │`               
->                `│                                              │`               
->                `│ When you are ready to continue, press ENTER. │`               
->                `│                                              │`               
->          25% c `└──────────────────────────────────────────────┘`               
->          ┌─────────────────────────────────────────────────────────┐          
->          │██████████████                                           │          
->          │██████████████                                           │          
->          └─────────────────────────────────────────────────────────┘          
->                                                                               
->                                                                               
->                                                                               
-> `ENTER=Continue  F3=Exit                                   │                 `

---

# 2. Tools of the trade

## 2.1 ASCII

-> * ███▄ ▄███▓▓██   ██▓    ▄▄▄▄    ▒█████    ██████   ██████ *
-> *▓██▒▀█▀ ██▒ ▒██  ██▒   ▓█████▄ ▒██▒  ██▒▒██    ▒ ▒██    ▒ *
-> *▓██    ▓██░  ▒██ ██░   ▒██▒ ▄██▒██░  ██▒░ ▓██▄   ░ ▓██▄   *
-> *▒██    ▒██   ░ ▐██▓░   ▒██░█▀  ▒██   ██░  ▒   ██▒  ▒   ██▒*
-> *▒██▒   ░██▒  ░ ██▒▓░   ░▓█  ▀█▓░ ████▓▒░▒██████▒▒▒██████▒▒*
-> *░ ▒░   ░  ░   ██▒▒▒    ░▒▓███▀▒░ ▒░▒░▒░ ▒ ▒▓▒ ▒ ░▒ ▒▓▒ ▒ ░*
-> *░  ░      ░ ▓██ ░▒░    ▒░▒   ░   ░ ▒ ▒░ ░ ░▒  ░ ░░ ░▒  ░ ░*
-> *░      ░    ▒ ▒ ░░      ░    ░ ░ ░ ░ ▒  ░  ░  ░  ░  ░  ░  *
-> *       ░    ░ ░         ░          ░ ░        ░        ░  *
-> *            ░ ░              ░                            *
-> * ██ ▄█▀ ██▓ ██▓     ██▓    ▓█████ ▓█████▄     ███▄ ▄███▓▓█████ *
-> * ██▄█▒ ▓██▒▓██▒    ▓██▒    ▓█   ▀ ▒██▀ ██▌   ▓██▒▀█▀ ██▒▓█   ▀ *
-> *▓███▄░ ▒██▒▒██░    ▒██░    ▒███   ░██   █▌   ▓██    ▓██░▒███   *
-> *▓██ █▄ ░██░▒██░    ▒██░    ▒▓█  ▄ ░▓█▄   ▌   ▒██    ▒██ ▒▓█  ▄ *
-> *▒██▒ █▄░██░░██████▒░██████▒░▒████▒░▒████▓    ▒██▒   ░██▒░▒████▒*
-> *▒ ▒▒ ▓▒░▓  ░ ▒░▓  ░░ ▒░▓  ░░░ ▒░ ░ ▒▒▓  ▒    ░ ▒░   ░  ░░░ ▒░ ░*
-> *░ ░▒ ▒░ ▒ ░░ ░ ▒  ░░ ░ ▒  ░ ░ ░  ░ ░ ▒  ▒    ░  ░      ░ ░ ░  ░*
-> *░ ░░ ░  ▒ ░  ░ ░     ░ ░      ░    ░ ░  ░    ░      ░      ░   *
-> *░  ░    ░      ░  ░    ░  ░   ░  ░   ░              ░      ░  ░*
-> *                                   ░                           *

^
-> *╔═══════════════════════════╗*
-> *║*  LIVE DEMO: Simple ASCII  *║*
-> *╚═══════════════════════════╝*


---

# 2. Tools of the trade

## 2.2 Unicode

0 1 2 3 4 5 6 7 8 9 : ; < =                                           > ? @ A B C D E F G H I J K L M N O P Q R S T

ɝ ɞ ɟ ɠ ɡ ɢ ɣ ɤ ɥ ɦ ɧ ɨ ɩ ɪ ɫ ɬ ɭ ɮ                                     ɯ ɰ ɱ ɲ ɳ ɴ ɵ ɶ ɷ ɸ ɹ ɺ ɻ ɼ ɽ ɾ ɿ ʀ ʁ ʂ ʃ ʄ

Ν Ξ Ο Π Ρ Σ Τ Υ Φ Χ Ψ                                                             δ ε ζ η θ ι κ λ μ ν ξ ο π ρ ς σ τ

Г Д Е Ж З И Й К Л М                                                                   О П Р С Т У Ф н о п р с т у ф

Ծ Կ Հ Ձ Ղ Ճ Մ Յ Ն Շ                                                         Ո Չ Պ Ջ Ռ Ս Վ Տ Ր Ց Ւ Փ Ք Օ Ֆ ՟ ա բ գ դ

ם מ ן נ ס ע                                                                                   ף פ ץ צ ק ר ש ת װ ױ ײ

د ذ ر ز س ش ص ض ط                                                                               ف ق ك ل م ن ه و ى ي
-> *Unicode*
झ ञ ट ठ ड ढ ण त थ द                                                                               ध न ऩ प फ ब भ म य

ஃ அ ஆ இ ஈ உ ஊ எ ஏ ஐ                                                                           க ங ச ஜ ஞ ட ண த ந ன ப

∍ ∏ ≠ ≡                                                                                 ≢ ≣ ≤ ≥ ≦ ≧ ≨ ≩ ≪ ≫ ≬ ≭ ≮ ≯

⌭ ⌮ ⌯ ⌰ ⌱ ⌲ ⌳ ⌴ ⌵ ⌶ ⌷ ⌸ ⌹ ⌺ ⌻                                                       ⍅ ⍆ ⍇ ⍈ ⍉ ⍊ ⍋ ⍌ ⍍ ⍎ ⍏ ⍐ ⍑ ⍒ ⍓ ⍔

ぎくぐけげこごさざしじすず                                                                   なにぬねのはばぱひびぴ

保俞俟俠信                                                                           俢俣俤俥俦俧俨俩俪俫俬俭修俯俰

---

# 2. Tools of the trade

## 2.2 Unicode





- Great addition

- Can provide creative tools

    - Braille

    - Special symbols

    - Block eighths

- Symbols not in monospace fonts

    - Fallback fonts used

    - Have to space out characters

---

# 2. Tools of the trade

## 2.2 Unicode

-> Some useful unicode symbols

^
-> Unicode block               Example symbols      Unicode range   
-> ──────────────────────────────────────────────────────────────── 
-> Block elements               ▁ ▂ ▃ ▅ ▆ ▇       0x2581 ... 0x2587 
-> 
->                              ▏ ▎ ▍ ▋ ▊ ▉       0x2589 ... 0x258f 
-> 
^
-> Enclosed Alphanumerics       ⑤ ⑸ ⒌ Ⓐ ⓐ ⓹       0x2460 ... 0x24ff 
-> 
^
-> Emoji, Dingbats, Misc.       😀 😁 😂 😃 😄 💩      [Multiple ranges](https://en.wikipedia.org/wiki/Emoji#Unicode_blocks)  
-> Symbols and Pictographs,                                         
-> ...                                                             

---

# 2. Tools of the trade

## 2.3 Basics of a terminal emulator

^
-> The VT100

->     \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
->    /                      \\   \\ 
->    |  .-----------.        |   |
->    |  |           |        |   |
->    |  |           |        |   |
->    |  |           |        |   |
->    |  |           |        |   |
->    |  \`-----------´  ====  |   |
->     \\\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_/\_\_\_'
->     /                      / / /
->    / \_/\_/\_/\_/\_/\_/\_/\_/\_/\_/ / / / 
->   / \_/\_/\_/\_/\_/\_/\_/\_/\_/\_/ /   /  
->  / \_/\_/\_/\_\_\_\_\_\_\_/\_/\_/\_/ / \_\_/   
-> /\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_/ /      
-> \\\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\\/       


---

# 2. Tools of the trade

## 2.3 Basics of a terminal emulator



- One of the first video *terminals* supporting _ANSI escape codes_

- Standard reference for all modern emulators

- Interface to host server

- Introduced box drawing characters, bold, blink, reverse...

- Cursor determines where text is printed

- Monospace fonts

- 1:2 character ratio

- Bi-directional communication

---

# 2. Tools of the trade

## 2.4 ANSI escape sequences



-> CSI (Control Sequence Introducer): `ESC  \[   `
->                                    `\\033 \[   `
->                                    `0x1b 0x5b`

-> Sequence         Function                                 
-> ──────────────────────────────────────────────────────────
-> CSI `n` (A|B|C|D)  Move cursor `n` blocks (up|down|right|left)
-> CSI (s|u)        (Save|restore) cursor position           
-> CSI ?25 (l|h)    (Hide|show) the cursor                   

-> CSI 2J           Clear screen                             
-> CSI `n` m          SGR (Select Graphic Rendition)           
-> CSI 38;5; `n` m    Set foreground color in 256-colors mode  
-> CSI ?47h         Use alternate screen buffer              

References: *http://invisible-island.net/xterm/ctlseqs/ctlseqs.html *
            *http://www.vt100.net/docs/ *
            *https://en.wikipedia.org/wiki/ANSI\_escape\_code *

^
-> *╔═══════════════════════════╗*
-> *║*  LIVE DEMO: Better ASCII  *║*
-> *╚═══════════════════════════╝*

---

# 2. Tools of the trade

## 2.5 Frameworks

^
*ncurses*: de facto library for most programs

^
- Not supported on windows

- Mainly *C*, but bindings exist

- Really _old API_, cumbersome for prototyping

^
In Python, litteral translation from C:

    
      # Init
      os.environ["ESCDELAY"] = "25"         # Reduce escape symbol timeout
      locale.setlocale(locale.LC_ALL, "")   # Force Unicode
    
      screen = curses.initscr()             # Initialize ncurses
    
      curses.noecho()                       # Don't print character inputs
      curses.raw()                          # Don't process inputs
      curses.start_color()                  # Enable colors
      curses.use_default_colors()           # Normal mode for colors
      curses.curs_set(0)                    # Hide cursor
    
      screen.timeout(33)                    # Make getting input non-blocking
    

---

# 2. Tools of the trade

## 2.5 Frameworks

    
      # Draw on screen
      curses.init_pair(1, 16, 0)
      pair = curses.color_pair(1)
      self.screen.addstr(5, 2, "Hello, World!".encode("utf-8"), pair)
    
^
      # Handle events
      ch = self.screen.getch()
      if ch in (27, 409):
          exit()
      elif event == -1:
          pass
      else:
          # React to event
          pass
    
^
      # Restore
      screen.keypad(False)
      curses.noraw()
      curses.echo()
      curses.endwin()
    

---

# 2. Tools of the trade

## 2.5 Frameworks





-> *                    █          *
-> *█▀█ █ █ █▀█ █▀▀ █▀█ █▀▄ █▀█ █▄█*
-> *█   █ █ █   ▀▀█ █▄█ █ █ █ █ ▄█▄*
-> *█▄█ █▄█ █   ▄▄█ █▄▄ █▄█ █▄█ █ █*

^
-> *Cursebox*, an open source simple curses wrapper
->  *https://github.com/Tenchi2xh/cursebox*

^
-> - Simple API with scoped block          

-> - Used in some of my projects           

-> - Still depends on curses               

-> - Helper utilities for converting colors

---

# 2. Tools of the trade

## 2.5 Frameworks



What does the same code look like this time?

^
    
      with Cursebox() as cb:
          # Draw on screen
          cb.put(5, 2, "Hello, World!",
                 fg=colors.white, bg=colors.black)
    
          # Handle events
          event = cb.poll_event()    
          if event in (EVENT_ESC, EVENT_CTRL_C):
              exit()
          elif event == EVENT_SKIP:
              pass
          else:
              # React to event
              pass
    

---

# 2. Tools of the trade

## 2.5 Frameworks







Scala framework:

- Nothing exists so far

- Implementation from scratch using ANSI escape sequences

- No curse dependency



^
-> *More details in a few slides ;)*

---

-> # 3. Delving deeper

->                                              ,--,  ,.-.      
->                ,                   \\,       '-,-\`,'-.' | .\_  
->               /|           \\    ,   |\\         }  )/  / \`-,',
->               [ ,          |\\  /|   | |        /  \\|  |/\`  ,\`
->               | |       ,.\`  \`,\` \`, | |  \_,...(   (      .', 
->               \\  \\  \_\_ ,-\` \`  ,  , \`/ |,'      Y     (   /\_L\\
->                \\  \\\_\\,\`\`,   \` , ,  /  |         )         \_,/
->                 \\  '  \`  ,\_ \_\`\_,-,<.\_.<        /         /   
->                  ', \`>.,\`  \`  \`   ,., |\_      |         /    
->                    \\/\`  \`,   \`   ,\`  | /\_\_,.-\`    \_,   \`\\    
->                -,-..\\  \_  \\  \`  /  ,  / \`.\_) \_,-\\\`       \\   
->                 \\\_,,.) /\\    \` /  / ) (-,, \`\`    ,        |  
->                ,\` )  | \\\_\\       '-\`  |  \`(               \\  
->               /  /\`\`\`(   , --, ,' \\   |\`<\`    ,            | 
->              /  /\_,--\`\\   <\\  V /> ,\` )<\_/)  | \\      \_\_\_\_\_) 
->        ,-, ,\`   \`   (\_,\\ \\    |   /) / \_\_/  /   \`----\`       
->       (-, \\           ) \\ ('\_.-.\_)/ /,\`    /                 
->       | /  \`          \`/ \\\\ V   V, /\`     /                  
->    ,--\\(        ,     <\_/\`\\\\     ||      /                   
->   (   ,\`\`-     \\/|         \\-A.A-\`|     /                    
->  ,>,\_ )\_,..(    )\\          -,,\_-\`  \_--\`                     
-> (\_ \\|\`   \_,/\_  /  \\\_            ,--\`                         
->  \\( \`   <.,../\`     \`-..\_\_\_\_\_,-\`                             

---


# 3. Delving deeper

## 3.1 Tiers of techniques

^
⠀                  ██            
⠀                 ██             
⠀                 ██             
⠀         █████   ██████   █████ 
⠀             ██  ██   ██ ██   ██
⠀        ████ ██  ██   ██ ██     
⠀        ██  ███  ██   ██ ██    █
⠀         ███ ██   █████   █████ 
^
⠀                                          ⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣶⠒⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀                                          ⠀⠀⠀⠀⠀⠀⠀⠀⢲⣿⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀                                          ⠀⢀⣠⣴⣶⡀⠀⠀⢸⣿⣇⣀⣴⣾⡀⠀⠀⣠⣤⣶⣦⠀⠀
⠀                                          ⣰⣿⠈⠙⣿⣿⠋⠀⢸⣿⡏⠀⢸⣿⣷⠀⣼⣿⠘⣿⣿⡷⠀
⠀                                          ⣿⣿⠀⠀⣿⣿⠀⠀⢸⣿⡇⠀⢸⣿⣿⠀⣿⣿⠀⠈⠁⠀⠀
⠀                                          ⣿⣿⠀⠀⣿⣿⠀⠀⢸⣿⡇⠀⢸⣿⣿⠀⣿⣿⠀⠀⠀⠀⠀
⠀                                          ⢿⣿⣄⠀⢿⣿⣤⠄⢾⣿⣷⣦⣸⣿⠇⠀⢿⣿⣷⣄⣀⠤⠂
⠀                                          ⠈⠟⠁⠀⠈⠟⠁⠀⠀⠈⠿⠛⠉⠁⠀⠀⠀⠻⠿⠋⠁⠀⠀
^
⠀                                                                                           ▄▄            
⠀                                                                                          ██             
⠀                                                                                          ██             
⠀                                                                                 ▄█▄▄▀█▄  ██▄▀█▄    ▄▀█▄ 
⠀                                                                                  ▄   ██  ██   ██ ▄█   ▀▀
⠀                                                                                 ██▀▄ ██  ██   ██ ██     
⠀                                                                                 ██  ▄██  ██   █▀ ██    ▄
⠀                                                                                  ▀▄▀ ▀█▀  ▀█▄▀    ▀█▄▄▀ 

---

# 3. Delving deeper

## 3.2 First generation

- 1:2 ratio
- 1 ppc
- 16 colors


- Dithering using characters: ░▒▓█

-> \     ▄ ▄ ▄   ▄▀▄▀▄▀▄  █▀█▀█▀█  ███████
-> \    ▄ ▄ ▄    ▄▀▄▀▄▀▄  ▀█▀█▀██  ███████
-> \     ▄ ▄ ▄   ▄▀▄▀▄▀▄  █▀█▀█▀█  ███████
-> \    ▄ ▄ ▄    ▄▀▄▀▄▀▄  ▀█▀█▀██  ███████
-> \     ▄ ▄ ▄   ▄▀▄▀▄▀▄  █▀█▀█▀█  ███████
-> \    ▄ ▄ ▄    ▄▀▄▀▄▀▄  ▀█▀█▀██  ███████
-> \     ▄ ▄ ▄   ▄▀▄▀▄▀▄  █▀█▀█▀█  ███████
-> \    ▄ ▄ ▄    ▄▀▄▀▄▀▄  ▀█▀█▀██  ███████

-> \      25%      50%      75%      100%


- Fake colors with foreground / background mixes

->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████
->  ░ ░ ░░░░▒░▒░▒▒▒▒▓▒▓▒▓▓▓▓█▓█▓██████
->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████
->  ░ ░ ░░░░▒░▒░▒▒▒▒▓▒▓▒▓▓▓▓█▓█▓██████
->   ░ ░░░░░░▒░▒▒▒▒▒▒▓▒▓▓▓▓▓▓█▓███████

---

# 3. Delving deeper

## 3.2 First generation

->               ██                                                         
->         ██  ██████  ██  * .d8b.  db                              db       *
->           ██████████    *d8' \`8b 88 .88b  d88. .d88b. .888b  .d8888 .d8888*
->     ██  ██████████████  *88ooo88 88 88  88  88 8P  Y8 88  88 88  88 \`8bo. *
-> ████████████████████    *88   88 88 88  88  88 8b  d8 88  88 88  8D   \`Y8b*
->     ██  ██████████████  *YP   YP YP YP  YP  YP \`Y88P' VP  VP Y888D' \`8888Y*
->           ██████████                                                     
->         ██  ██████  ██    T e r m i n a l   f r a c t a l   v i e w e r  
->               ██                                                         

- Python
- Explore the Mandelbrot / Julia fractals
- Custom cross-platform ncurses-like library
- Basic UI widgets
- High resolution exports

- Open source: *https://github.com/Tenchi2xh/Almonds*

^
-> *╔══════════════════════╗*
-> *║*  LIVE DEMO: Almonds  *║*
-> *╚══════════════════════╝*

---

# 3. Delving deeper

## 3.3 Second generation

- 1:1 ratio

- 8 ppc

- Monochrome

^
-> [Pixel to unicode braille encoding ®](Patent pending [not really])

^
-> ██          *①*  ④                  
->   ██        ②  *⑤*                  
-> ████   ──>  *③  ⑥*   ──>  0b10101110
-> ██          *⑦*  ⑧                  

-> Pixels     Unicode    Raised dots 
->            braille     as binary  
->             order                 

^
-> ──> 0b01110101 + 0x2800 = 0x2875
-> \       Reverse and add offset   

^
-> ──>  *⡵*  Braille character result

^
-> *1:1 mapping* of *pixels* to characters

---

# 3. Delving deeper

## 3.3 Second generation




->          ⢀⣤⣴⣶⣶⣶⣶⣶⣶⣶⣶⣦⣄⡀                                                                                            
->         ⣰⣿⠟⠛⠻⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣆                                                     ⣶⣾                                    
->         ⣿⣿⣀ ⣠⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿                                               ⣀     ⣿⣿                                    
->         ⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿                                             ⢸⣿⣿     ⣿⣿                                    
->  ⣀⣤⣤⣤⣤⣤⣤⣤⣤⣤⣤⣤⣤⣤⣤⣿⣿⣿⣿⣿⣿⣿⣿ *⣤⣤⣤⣤⣄⡀*                                      ⢸⣿⣿     ⣿⣿                                    
-> ⣼⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿ *⣿⣿⣿⣿⣿⣿⡆*        ⢀⣤⣶⠿⠿⠛⠿⢿⣷⣦⡀   ⣶⣿⡇      ⢸⣿⡇  ⠿⢿⣿⣿⠿⠿⠇  ⣿⣿⣠⣴⣶⠿⠿⣿⣷⣦⡀    ⣠⣶⡿⠿⠿⠿⣷⣦⡀    ⣠⣶⡿⠿⠛⠻⠿⣿⣦⡀
-> ⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡿ *⣿⣿⣿⣿⣿⣿⣿*        ⣿⣿⠁     ⠹⣿⣷   ⣿⣿⡇      ⢸⣿⡇   ⢸⣿⣿     ⣿⣿⠛⠁    ⢻⣿⣷  ⢀⣾⣿⠋    ⠈⢻⣿⣆  ⢸⣿⡏     ⠈⣿⣿
-> ⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠟⠁*⣼⣿⣿⣿⣿⣿⣿⣿*        ⣿⣿       ⣿⣿⡇  ⣿⣿⡇      ⢸⣿⡇   ⢸⣿⣿     ⣿⣿      ⠈⣿⣿  ⣼⣿⡇      ⠈⣿⣿⡄ ⢸⣿⡇      ⣿⣿
-> ⣿⣿⣿⣿⣿⣿⣿⣿⡿⠛⠁          *⣠⣴⣿⣿⣿⣿⣿⣿⣿⣿⣿*        ⣿⣿       ⣿⣿⡇  ⣿⣿⡇      ⢸⣿⡇   ⢸⣿⣿     ⣿⣿       ⣿⣿  ⣿⣿⡇       ⣿⣿⡇ ⢸⣿⡇      ⣿⣿
-> ⣿⣿⣿⣿⣿⣿⣿⠏*⢠⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿*        ⣿⣿       ⣿⣿⡇  ⣿⣿⡇      ⢸⣿⡇   ⢸⣿⣿     ⣿⣿       ⣿⣿  ⢹⣿⣧      ⢀⣿⣿⠁ ⢸⣿⡇      ⣿⣿
-> ⣿⣿⣿⣿⣿⣿⣿ *⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿*        ⣿⣿⣀    ⢀⣼⣿⡿   ⢹⣿⣧⡀    ⢀⣼⣿⡇   ⠸⣿⣿     ⣿⣿       ⣿⣿  ⠈⢻⣿⣆    ⢀⣼⣿⠋  ⢸⣿⡇      ⣿⣿
-> ⠹⣿⣿⣿⣿⣿⣿ *⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠇*        ⣿⣿⠛⠿⢷⣶⣶⣿⠿⠋     ⠙⠿⣿⣷⣶⡶⠿⠟⢻⣿⡇    ⠙⠿⣷⣶⡄  ⠿⠿       ⠿⠿    ⠙⠿⢷⣶⣶⣶⠿⠛⠁   ⠸⠿⠇      ⠿⠿
->  ⠈⠙⠛⠛⠛⠛ *⣿⣿⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⠉*          ⣿⣿                     ⢸⣿⡇                                                 
->         *⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿*                ⣿⣿                    ⢀⣿⡿                                                  
->         *⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠁ ⠈⣿⣿*                ⣿⣿                ⣠⣤⣤⣶⡿⠟⠁                                                  
->         *⠙⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣦⣤⣴⡿⠃*                ⠈⠉                ⠉⠉⠉                                                      
->           *⠉⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⠉*                                                                                             

---

# 3. Delving deeper

## 3.3 Second generation

-> ┌─────────────────────────────────────┐
-> │⠀⠀⠀⠀⢠⡼⣻⣇⣀⠀⠀⠀⠀⠀⠀⠀⠙*⣀⠴⠊⠁*⡍⢿⡀⠀⠀⠀⢻⠋⠁⠀⠀⢀⣤⡘⣲⠤│
-> │⠀⠀⠀⣀⣙⣷⠤⠶⢧⠀⠀⠀⠀⠀*⢀⡤⠚⠁*⠀⡏⣠⠗⠀⢻⣀⡤⠴⠋⠀⠀⠀⢀⣷⠒⠚⠓⠲│
-> │⣰⡾⠛⠻⡽⠛⢉⣿⠀⠑⣦⠀*⢀⠴⠋*⠀⢀⣀⣀⣿⣟⠲⠦⠒⠢⣤⠔⠒⠊⠓⠺⠛⠛⠛⢦⠤⠴│
-> │⣾⣟⡤⠤⠇⢼⣟⣀⡄⠀*⣠⣶⠥⠤⠴⠲⠄*⠼⠁⠀⠀⠀⠀⠀⠀⢳⠀⠀⠀⠀⠀⠀⠀⠀⢾⣁⠤│
-> │⠀⠀⠀⠀⠠⠾⠽⠛⢒⣚⣒⣩⠏⠙⠫⠤⣹⣄⠀⠀⠀⠀⠀⣖⠒⠋⠉⠲⠲⣄⣀⠀⣀⢀⡬⠃⠀│
-> │⠀⠀⠀⠀⠀⠰⣶⣓⡒⠃⠀⠀⠀⠀⠀⠀⠀⢈⣹⣃⣀⣀⣀⣨⡟⠒⠉⣳⠮⣅⠤⠽⠓⣿⠥⢄⣠│
-> │⠀⠀⠀⠀⠀⠀⠀⠀⠙⣦⠀⠀⠀⠀⠀⠀⠠⢿⡤⠦⠿⠟⠉⣓⣶⣒⣲⠟⢤⣠⡤⢤⡞⠀⠀⠀⠀│
-> │⠀⠀⣀⣀⣀⣀⣀⣀⣀⡏⠀⠀⠀⠀⢀⡀⠀⢸⣤⠴⠤⡀⠀⠧⣘⠙⢾⣯⡉⠙⣯⠀⠙⢲⣄⣀⣀│
-> │⠀⢻⣤⣤⡉⠉⠉⠉⠉⠉⠒⠒⠶⣾⠁⠉⠉⠉⠀⠀⠀⠙⠤⣀⠈⠣⣤⡉⠛⠺⢽⢧⠤⠼⡁⣀⡀│
-> │⠀⣸⠀⣸⠁⠀⠀⠀⠀⠀⢠⠞⠉⠀⠀⠀⠀⠀⠀⡏⢳⠀⠀⠈⠙⠲⢤⣹⠶⡤⢾⣨⠛⠹⡿⡿⠛│
-> │⠀⢷⠀⡟⠀⠀⠀⠀⠀⢀⡝⠀⠀⠀⠀⠀⠀⠀⠀⠋⠉⠀⠀⣠⡤⠤⣤⡟⠃⠀⠀⠙⣧⣴⣯⡄⠀│
-> │⠀⠘⠉⠉⢢⣤⠒⠒⠚⢉⣀⡤⠖⠒⠒⠒⠒⠓⠒⡞⠉⢶⠀⠈⠉⠒⠃⠀⠀⠀⠀⠀⠙⠺⠏⠀⠀│
-> │⠀⠀⠀⣠⠏⠈⠉⠉⠻⡅⠀⠀⠀⠀⠀⠀⠀⠀⣠⠃⠀⡜⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀│
-> └─────────────────────────────────────┘
-> Surveyor

- Python
- Parses `traceroute` outputs
- Matches IPs with locations (via GeoIP database)

^
-> *╔═══════════════════════╗*
-> *║*  LIVE DEMO: Surveyor  *║*
-> *╚═══════════════════════╝*

---

# 3. Delving deeper

## 3.4 Third generation

- 1:1 ratio

- 2 ppc

- 256-colors


^
"Real pixels" trick:

- ▀ character (upper half block)

- Full character block ratio is 1:2

- Half block is 1:1 (square pixels)

- Upper pixel color via *foreground*

- Lower pixel color via *background*


^
-> *1:1 mapping* of *pixels* to characters

---

# 3. Delving deeper

## 3.4 Third generation

- `xterm256` mode has 256 arbitrary colors

- Convert `xterm256` codes to RGB tuples

- Compute [gamma adjusted distance](Nice explanation by MinutePhysics: https://youtu.be/LKnqECcg6Gw) between target and all `xterm256` colors

-> Distance between two colors:

-> √([r0 - r1]² + [g0 - g1]² + [b0 - b1]²)

- Dynamic memoized lookup table


^
-> *1:1 mapping* of *colors* to `xterm256` codes

---

# 3. Delving deeper

## 3.4 Third generation




Less pixels than generation?

- Braille had more pixels par character

- No colors

- Generation 3 is a real *pixel buffer*

- “Turing completeness” of graphics


^
-> *1:1 mapping* of _*pixels and colors*_ to characters

---

# 3. Delving deeper

## 3.4 Third generation

->                                 .::.                          
->                               .;:**'                          
->                               \`                               
->   .:XHHHHk.              db.   .;;.     dH  MX                
-> oMMMMMMMMMMM       ~MM  dMMP :MMMMMR   MMM  MR      ~MRMN     
-> QMMMMMb  "MMX       MMMMMMP \!MX' :M~   MMM MMM  .oo. XMMM 'MMM
->   \`MMMM.  )M> :X\!Hk. MMMM   XMM.o"  .  MMMMMMM X?XMMM MMM>\!MMP
->    'MMMb.dM\! XM M'?M MMMMMX.\`MMMMMMMM~ MM MMM XM \`" MX MMXXMM 
->     ~MMMMM~ XMM. .XM XM\`"MMMb.~\*?\*\*~ .MMX M t MMbooMM XMMMMMP 
->      ?MMM>  YMMMMMM\! MM   \`?MMRb.    \`"""   \!L"MMMMM XM IMMM  
->       MMMX   "MMMM"  MM       ~%:           \!Mh.""" dMI IMMP  
->       'MMM.                                             IMX   
->        ~M\!M                                             IMP   
-> *pokedex-cli*

- Pokémon encyclopedia
- Queries a sqlite database (Veekun)
- Renders sprites from the game

- Open source: *https://github.com/Tenchi2xh/pokedex-cli*

^
-> *╔══════════════════════╗*
-> *║*  LIVE DEMO: Pokedex  *║*
-> *╚══════════════════════╝*

---

# 3. Delving deeper

## 3.4 Third generation




-> *⣿ ⣤ ⣀ ⣀ ⣀ ⣀ ⣀ ⠀ ⠀ ⠀ ⠀ ⣀ ⣤ ⣿ ⣤ ⠀ ⠀ ⠀ ⠀ ⣀*
-> ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣶ ⣶ ⣿ ⣿ ⣿ ⣿ ⣿ ⣤ ⣤ ⣶ ⣿
-> ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿
-> ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿ ⣿

-> *Orbiter*

- Python

- Old-school module player

- Binding to OpenMPT C library via `ctypes`

- Live visualizations in the terminal

- Spectrum analysis with FFT

^
-> *╔══════════════════════╗*
-> *║*  LIVE DEMO: Orbiter  *║*
-> *╚══════════════════════╝*

---

# 3. Delving deeper

## 3.4 Third generation


-> Next project
-> Featured in the 

-> `┌────────────────┐`
-> `│ 𝕾 𝖈𝖆𝖑𝖆 𝕿 𝖎𝖒 𝖊𝖘 │`
-> `│ ══════════════ │`
-> `│ ☴☱☲  ☶☱☱  ☱☰☲  │`
-> `│ ▄▄▄▄ ☱☰☲  ☱☱☶  │`
-> `│ ▒▓█▓ ☳☱☰  ☴☶☵  │`
-> `└────────────────┘`



^
-> Unicode block               Example symbols      Unicode range  
-> ────────────────────────────────────────────────────────────────
-> Mathematical Alphanumeric   𝕬 𝕭 𝕮 ... 𝖝 𝖞 𝖟   0x1d56c ... 0x1d59f
-> Symbols, Fraktur Bold                                           
->                                                                 
-> Miscellaneous Symbols,      ☰ ☱ ☲ ☳ ☴ ☵ ☶ ☷   0x02630 ... 0x02637
-> Chinese Cosmology Trigrams                                      

---

# 3. Delving deeper

## 3.4 Third generation

-> *Scurses*

^
- Easy to use Curses-like framework for *Scala*
- From scratch: *no dependencies*

- Open source: *https://github.com/Tenchi2xh/Scurses*

    
      import net.team2xh.scurses.{Scurses, Colors}
      
      object HelloWorld extends App {
        Scurses { screen =>
          val (w, h) = screen.size
          val prompt = "Press a key to continue..."
          screen.put(w/2 - prompt.length/2, h/2 + 1, prompt, Colors.BRIGHT_BLACK)
          screen.refresh()
          screen.keypress()
        }
      }
    

^
-> *╔══════════════════════╗*
-> *║*  LIVE DEMO: Scurses  *║*
-> *╚══════════════════════╝*

---

# 3. Delving deeper

## 3.4 Third generation

-> *Onions*

^
- *UI* framework based on Scurses

- Recursive tiling layout

- Multiple extendable widgets

  - Graphs (histograms, bars, plots, heatmaps)
  - Big text fonts
  - Radio, checkbox
  - Justifiable labels
  - Image buffer

- Observable widgets

- Open source: *https://github.com/Tenchi2xh/Scurses*

^
-> *╔═════════════════════╗*
-> *║*  LIVE DEMO: Onions  *║*
-> *╚═════════════════════╝*

---

# 3. Delving deeper

## 3.4 Third generation

-> *Svordom*

- 3D ray casting maze

- Dynamic palette adjustment

- Dithering and anti-aliasing

- Scrolling text

- Built-in texture editor

^
-> *╔══════════════════════╗*
-> *║*  LIVE DEMO: Svordom  *║*
-> *╚══════════════════════╝*

---





->              O            
->            .oOo.          
->         .oOOOOOOOo.       
->      .OOOOOOOOOOOOOOo.    
->     oOOOOOOOOOOOOOOOOOo   
->     OOOOOOOOOOOOOOOOOOO   
->     oOOOOOOOOOOOOOOOOOo   
->      'oOOOOOOOOOOOOOo'    
->     ...  'oOOOOOo'  ...   
->  .oOOOOOo. oOOOo .oOOOOOo.
-> oOOOOOOOOOo OOO oOOOOOOOOo
-> OOOo  \`oOOOOOOOOOOo'  oOOO
->  oOo    oOOOOOOOOo    oOo 
->        #############      
->          oo oOo oo        
->      Ooooo oOOOo ooooO    
->       \`"\` OOOOOOO \`"\`     
->            'oOo'          


-> Thank you \!

---







->    .oOOOOOOOOo.    
->   oOOOOOOOOOOOOo.  
->  OOOO'      'OOOO. 
-> OOOO'        'OOOO 
-> 'OO'         .OOOO 
->            .oOOO'  
->           .OOOO'   
->         .OOOO'     
->        .OOOO'      
->        OOOO'       
->        OOOO        
->        'OO'        
->                    
->        .OO.        
->        OOOO        
->        'OO'        


-> Questions ?

