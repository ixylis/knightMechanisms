# knightMechanisms

Alpha-beta chess engine designed to act as an introduction to game tree decisions. 

# Compilation and Execution

` $ cd chess-engine`  
` $ g++ src/source.cpp src/*/*.cpp -o chess`
` $ ./chess <args>`

```
 <arg1> - Type of Game
  1. Human vs. Computer
  2. Computer vs. Human
  3. Computer vs. Computer
 <arg2> - Depth for Tree Search
  - some integer value >0
```

# How to Play

Choose a move by declaring the square the piece will move from to the square that the piece will move to. 

# Performance

While the performance is system specific, using a depth of `[1, 4]` results in very speedy AI decision and with a depth of `5` having adequate speed. The program can accept any depth greater than `0`, although the depth which NegaMax search uses is one plus this number (eg. using a depth of `1` searches 1 ply beyond available moves). Timing using a Ryzen 3600 for moves is below:

| Depth | Early Game | Middle Game | Late Game | Average   |
| ----- | ---------- | ----------- | --------- | --------- |
| 1     | 1.8msec    | 1.0msec     | 1.4msec   | 1.3msec   |
| 2     | 3.9msec    | 3.4msec     | 1.9msec   | 3.0msec   |
| 3     | 67.9msec   | 117.9msec   | 111.7msec | 96.7msec  |
| 4     | 396.9msec  | 354.8msec   | 121.1msec | 298.2msec |
| 5     | 5.0sec     | 1.2sec      | 0.4sec    | 1.7sec    |
| 6     | 13.9sec    | 24.5sec     | 10.2sec   | 22.6sec   |
| 7     | 630.4sec   | 112.6sec    | 41.9sec   | 163.4sec  |

# Improvements

- Adding a GUI
- Implementing En Passant
- Opening Dictionary

