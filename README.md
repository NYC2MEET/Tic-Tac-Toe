# Tic-Tac-Toe
c++ code
#include<iostream>
#include<cstdlib>
#include<conio.h>
using namespace std;
#include<string>
int j;
int n=0;
char symbol;


char square[10] = {'o','1','2','3','4','5','6','7','8','9'};
void board()
{
    system("cls");
    cout << "\n\n\tTic Tac Toe\n\n";

    cout << "Player 1 (X)  -  Player 2 (O)" << endl << endl;
    cout << endl;

    cout << "     |     |     " << endl;
    cout << "  " << square[1] << "  |  " << square[2] << "  |  " << square[3] << endl;

    cout << "_____|_____|_____" << endl;
    cout << "     |     |     " << endl;

    cout << "  " << square[4] << "  |  " << square[5] << "  |  " << square[6] << endl;

    cout << "_____|_____|_____" << endl;
    cout << "     |     |     " << endl;

    cout << "  " << square[7] << "  |  " << square[8] << "  |  " << square[9] << endl;

    cout << "     |     |     " << endl << endl;
}
void board(char square[])
{
    system("cls");
    cout << "\n\n\tTic Tac Toe\n\n";

    cout << "Player 1 VS Computer " << endl << endl;
    cout << endl;

    cout << "     |     |     " << endl;
    cout << "  " << square[1] << "  |  " << square[2] << "  |  " << square[3] << endl;

    cout << "_____|_____|_____" << endl;
    cout << "     |     |     " << endl;

    cout << "  " << square[4] << "  |  " << square[5] << "  |  " << square[6] << endl;

    cout << "_____|_____|_____" << endl;
    cout << "     |     |     " << endl;

    cout << "  " << square[7] << "  |  " << square[8] << "  |  " << square[9] << endl;

    cout << "     |     |     " << endl << endl;
}
int checkwin()
{
    if (square[1] == square[2] && square[2] == square[3])

        return 1;
    else if (square[4] == square[5] && square[5] == square[6])

        return 1;
    else if (square[7] == square[8] && square[8] == square[9])

        return 1;
    else if (square[1] == square[4] && square[4] == square[7])

        return 1;
    else if (square[2] == square[5] && square[5] == square[8])

        return 1;
    else if (square[3] == square[6] && square[6] == square[9])

        return 1;
    else if (square[1] == square[5] && square[5] == square[9])

        return 1;
    else if (square[3] == square[5] && square[5] == square[7])

        return 1;
    else if (square[1] != '1' && square[2] != '2' && square[3] != '3' 
                    && square[4] != '4' && square[5] != '5' && square[6] != '6' 
                  && square[7] != '7' && square[8] != '8' && square[9] != '9')

        return 0;
    else
        return -1;
}
int checkwins(char board[])
{
    if (square[1] == square[2] && square[2] == square[3])

        return 1;
    else if (square[4] == square[5] && square[5] == square[6])

        return 1;
    else if (square[7] == square[8] && square[8] == square[9])

        return 1;
    else if (square[1] == square[4] && square[4] == square[7])

        return 1;
    else if (square[2] == square[5] && square[5] == square[8])

        return 1;
    else if (square[3] == square[6] && square[6] == square[9])

        return 1;
    else if (square[1] == square[5] && square[5] == square[9])

        return 1;
    else if (square[3] == square[5] && square[5] == square[7])

        return 1;
    else if (square[1] != '1' && square[2] != '2' && square[3] != '3' 
                    && square[4] != '4' && square[5] != '5' && square[6] != '6' 
                  && square[7] != '7' && square[8] != '8' && square[9] != '9')

        return 0;
    else
        return -1;
}



int main()
{
    int players,computer;


    cout<<"IF YOU WANT TWO PLAYER MODE OR COMPUTER\n1.COMPUTER MODE PRESS 1\n2.TWO PLAYER MODE PRESS 2";
    cin>>players;
    if(players==1)
    {
        cout<<"\tCOMPUTER MODE";
        int mode,i,q,m=0;
	char symbol;
	while(m!=-1)
	{
		system("cls");
		cout<<"\nDo you want the first move?If you want click 1 otherwise click 2\n";
		cin>>mode;
		if((mode!=1)&&(mode!=2))
		{
			cout<<"\nINVALID NUMBER CLICK A CORRECT  NUMBER"<<endl;
		}
		else
		{
			m=-1;
		}
	}
		while(m!=1)
		{
			system("cls");
			cout<<"\nENETR A CHARACTER PLEASE ENTER A CAPS";
			cin>>symbol;
			if((symbol!='X')&&(symbol!='O'))
			{
				cout<<"\nINVALID CHARACTER";
			}
			else
			{
				m=1;
			}
		}
		do{
			board(square);
			if(mode % 2==1)
			mode=1; 
			else
			mode=2;
			if(mode==2)
			{
				cout<<"PLAYERS"<<mode<<endl;
				cout<<"PRESS ENTER KEY ON KEYBOARD FOR PLAY COMPUTER"<<endl;
				q=rand()%9;
				if(symbol=='X')
				  symbol='O';
				  else if(symbol=='O')
				  symbol='X';
				  int turn=1;
				  int placed=0;
				  while(placed==0)
				  {
				   if (q == 1 && square[1] == '1')
				   {
				   

                    square[1] = symbol;
                    placed=1;
                }
        else if (q == 2 && square[2] == '2')
        {
		

            square[2] = symbol;
            placed=1;
        }
        else if (q == 3 && square[3] == '3')
        {
		

            square[3] = symbol;
            placed=1;
        }
        else if (q == 4 && square[4] == '4')
        {
		

            square[4] = symbol;
            placed=1;
        }
        else if (q == 5 && square[5] == '5')
        {
		

            square[5] = symbol;
            placed=1;}
        else if (q == 6 && square[6] == '6')
        {
		

            square[6] = symbol;
            placed=1;
        }
        else if (q == 7 && square[7] == '7')
        {
		

            square[7] = symbol;
            placed=1;
        }
        else if (q == 8 && square[8] == '8')
        {
		

            square[8] = symbol;
            placed=1;
        }
        else if (q == 9 && square[9] == '9')
        {
		

            square[9] = symbol;
            placed=1;
        }
            else
            {
			
             q=rand()%9;
         }
				  }
				  i=checkwins(square);
				  mode++;
				  _getche();
				  board(square);
			}
			else if(mode==1)
			{
				if(symbol=='X'){
					symbol='O';
				}
				else if(symbol='O')
				{
					symbol='X';
				}
				n=1;
				cout<<"\nplayers\t"<<mode<<"enter a choice "<<endl;
				cin>>q;
				if (q == 1 && square[1] == '1')
				   {
				   

                    square[1] = symbol;
                    ;
                }
        else if (q == 2 && square[2] == '2')
        {
		

            square[2] = symbol;
            ;
        }
        else if (q == 3 && square[3] == '3')
        {
		

            square[3] = symbol;
            ;
        }
        else if (q == 4 && square[4] == '4')
        {
		

            square[4] = symbol;
            ;
        }
        else if (q == 5 && square[5] == '5')
        {
		

            square[5] = symbol;
            }
        else if (q == 6 && square[6] == '6')
        {
		

            square[6] = symbol;
            
        }
        else if (q == 7 && square[7] == '7')
        {
		

            square[7] = symbol;
            
        }
        else if (q == 8 && square[8] == '8')
        {
		

            square[8] = symbol;
            
        }
        else if (q == 9 && square[9] == '9')
        {
		

            square[9] = symbol;
            
        } 
        else{
        	cout<<"INVALID MOVE";
        	mode--;
        	_getche();
		}
		i=checkwins(square);
		mode++;
				
			}
		}while(i==-1);
		board(square);
		if(i==1)
		{
			cout<<"\n CONGRATULATIONS! \nPlayer"<<--mode<<"wins";
		}
		else
		{
			cout<<"\nGAME DRAWN"<<endl;
		}
		system("pause");
		getche();
	
	
        
        
    }
    if(players==2)
    {
        int player = 1,i,choice;

    char mark;
    do
    {
        board();
        player=(player%2)?1:2;

        cout << "Player " << player << ", enter a number:  ";
        cin >> choice;

        mark=(player == 1) ? 'X' : 'O';

        if (choice == 1 && square[1] == '1')

            square[1] = mark;
        else if (choice == 2 && square[2] == '2')

            square[2] = mark;
        else if (choice == 3 && square[3] == '3')

            square[3] = mark;
        else if (choice == 4 && square[4] == '4')

            square[4] = mark;
        else if (choice == 5 && square[5] == '5')

            square[5] = mark;
        else if (choice == 6 && square[6] == '6')

            square[6] = mark;
        else if (choice == 7 && square[7] == '7')

            square[7] = mark;
        else if (choice == 8 && square[8] == '8')

            square[8] = mark;
        else if (choice == 9 && square[9] == '9')

            square[9] = mark;
        else
        {
            cout<<"Invalid move ";

            player--;
            cin.ignore();
            cin.get();
        }
        i=checkwin();

        player++;
    }while(i==-1);
    board();
    if(i==1)

        cout<<"==>\aPlayer "<<--player<<" win ";
    else
        cout<<"==>\aGame draw";

    cin.ignore();
    cin.get();
    return 0;
}
    }
