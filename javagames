import java.util.Scanner;

class Tictactoe {
  public static void main(String[] args) {
    char[][] board = new char[3][3];
    for (int row = 0; row < board.length; row++) {
      for (int col = 0; col < board[row].length; col++) {
        board[row][col] = ' ';
      }
    }

    char player = 'X';
    boolean gameover = false;
    Scanner sc = new Scanner(System.in);

    while (!gameover) {
      printboard(board);
      System.out.print("Player " + player + " Enter: ");
      int row = sc.nextInt();
      int col = sc.nextInt();

      if (board[row][col] == ' ') {
        // place the element
        board[row][col] = player;
        gameover = havewon(board, player);
        if (gameover) {
          System.out.println("Player " + player + " Has won");

        } else {
          if (player == 'X') {
            player = 'O';
          } else {
            player = 'X';
          }
        }

      }
      // else if(row>2||col>2){
      // System.out.println("You are exceding the limit of rows ");
      // continue;
      // }
      else {
        System.out.println("Invalid move");
      }

    }
    printboard(board);

  }

  public static boolean havewon(char[][] board, char player) {
    // check the rows
    for (int row = 0; row < board.length; row++) {
      if (board[row][0] == player && board[row][1] == player && board[row][2] == player) {
        return true;
      }

    }
    // check for the column
    for (int col = 0; col < board.length; col++) {
      if (board[0][col] == player && board[1][col] == player && board[2][col] == player) {
        return true;
      }

    }

    // diagonal checkup
    if (board[0][0] == player && board[1][1] == player && board[2][2] == player) {
      return true;
    }
    if (board[0][2] == player && board[2][2] == player && board[2][0] == player) {
      return true;
    }

    return false;
  }

  public static void printboard(char[][] board) {
    for (int row = 0; row < board.length; row++) {
      for (int col = 0; col < board[row].length; col++) {
        System.out.print(board[row][col] + " |");
      }
      System.out.println();
    }
  }
}
