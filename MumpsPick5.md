PICK5∙  ;LOTTERY GAME.  USER GUESSES 5 NUMBERS BETWEEN 1 AND 20.  ANY MATCHING [
 09/28/2015  8:27 PM ]←
∙       ;NUMBERS RESULT IN A CASH PRIZE.  TRY AND GET A JACKPOT!←
∙       S MATCHED=0←
∙       W "WELCOME TO PICK-5! (NUMBERS ARE BETWEEN 0 AND 20!)",!←
∙       H 3←
∙       W "GENERATING LOTTO NUMBERS"←
∙       H 1←
∙       W "."←
∙       H 1←
∙       W "."←
∙       H 1←
∙       W ".",!!←
∙       H 1←
∙       S LOTTO1=$R(20)+1 S LOTTO2=$R(20)+1 S LOTTO3=$R(20)+1 S LOTTO4=$R(20)+1
S LOTTO5=$R(20)+1←
∙       W "GUESS FIRST NUMBER: " R NUM1 ←
∙       W !!,"GUESS SECOND NUMBER: " R NUM2←
∙       W !!,"GUESS THIRD NUMBER: " R NUM3←
∙       W !!,"GUESS FOURTH NUMBER: " R NUM4←
∙       W !!,"GUESS FIFTH NUMBER: " R NUM5 W !!←
∙       ←
SHOW∙   W "YOUR NUMBERS      LOTTO NUMBERS",!←
∙       W "     " W NUM1 W "                 " W LOTTO1 W !←
∙       W "     " W NUM2 W "                 " W LOTTO2 W !←
∙       W "     " W NUM3 W "                 " W LOTTO3 W !←
∙       W "     " W NUM4 W "                 " W LOTTO4 W !←
∙       W "     " W NUM5 W "                 " W LOTTO5 W !←
∙       ←
COMPARE∙I NUM1=LOTTO1 D MATCH←
∙       ←
∙       I NUM2=LOTTO2 D MATCH←
∙       ←
∙       I NUM3=LOTTO3 D MATCH←
∙       ←
∙       I NUM4=LOTTO4 D MATCH←
∙       ←
∙       I NUM5=LOTTO5 D MATCH←
∙       ←
TOTAL∙  I MATCHED=0 W "NO MATCHES!  PLAY AGAIN!",!←
∙       I MATCHED=1 W "1 MATCH! YOU WIN $100!",!←
∙       I MATCHED=2 W "2 MATCHES! YOU WIN $1,000!",!←
∙       I MATCHED=3 W "3 MATCHES! YOU WIN $10,000!!",!←
∙       I MATCHED=4 W "4 MATCHES! WOW! YOU WIN $100,000!!",!←
∙       I MATCHED=5 W "JACKPOT!! YOU WIN 1 MILLION DOLLARS!!",!←
∙       ←
∙       D PICK5←
∙       ←
MATCH∙  S MATCHED=MATCHED+1←
