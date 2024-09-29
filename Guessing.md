#Guessing Game

##generate random number between 1 and 10
```mermaid
flowchart TD;
setup-dev((Winning number randomized))
bci((Prompt 1 integer guess))
bci-lima((validate guess))
bci-high((too high))
bci-quatro((too low))
bci-cinco((Winner))
setup-dev-->bci
bci-->bci-lima
bci-lima-->bci-high
bci-lima-->bci-quatro
bci-lima-->bci-cinco
bci-high-->bci
bci-quatro-->bci






