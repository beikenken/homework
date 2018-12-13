# 智能蛇实验报告

     char BLANK_CHAR = ' ';
     char WALL_CHAR = '*';
     char SNAKE_HEAD_CHAR = 'H';
     char SNAKE_BODY_CHAR = 'X';
     har FOOD_CHAR = '$';
     char map[12][13] = {
     "************",
     "*          *", 
     "*          *",
     "*          *", 
     "*          *",  
     "*          *", 
     "*          *", 
     "*          *",  
     "*          *",  
     "*          *",  
     "*          *",  
     "************",
     };
     int snakeHeadX = 1, snakeHeadY = 1;
     int snakeBodyX[100] = {0}, snakeBodyY[100] = {0};
     int snakeBodyLen = 0;
     int snakeTailIndex = -1;
     int willBeLonger = 0;
     int foodX = 0, foodY = 0;
     int gameRunning = 1;
     void snakeMove(char control){
     map[snakeHeadX][snakeHeadY]=
     BLANK_CHAR; // record the previous snake head position int prevSnakeHeadX=
     snakeHeadX; int prevSnakeHeadY=
    snakeHeadY; 
    switch(control){ 
    case'w':    snakeHeadX--;   
    break;  
    case'a':   
    snakeHeadY--;   
    break;  case's':   
    snakeHeadX++;  
    break; 
    case'd':    
    snakeHeadY++; 
    break;  
    default:   
    return; } 
    if(map[snakeHeadX][snakeHeadY]!=BLANK_CHAR&&map[snakeHeadX][snakeHeadY]!=FOOD_CHAR) {
    gameOver();
    }

