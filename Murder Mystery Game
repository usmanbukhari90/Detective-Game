#include <iostream>
#include <conio.h>
#include <cstdlib>
#include <ctime>
#include <iomanip>
#include <math.h>
#include <algorithm>
#include <ctime>
using namespace std;
bool visited[6] = {false};
void clue(int choice, int score, int energytotal, int culprit);
int energytotal = 100, score = 0;
void summary(int energytotal, int score)
{

    cout << "Your Energy after this investigation is: " << energytotal << endl;
    cout << "Your Reputation after this investigation is: " << score << endl;
    cout << "-------------------------------------" << endl;
    cout << "             GOOD BYE!" << endl;
    cout << "-------------------------------------" << endl;
    exit(0);
}
void investigation(int choice)
{
    switch (choice)
    {
    case 4:
        cout << "-------------------------------------" << endl;
        cout << "Reply by Sophine Maid" << endl;
        cout << "I am not Culprit" << endl;
        cout << "I dont even know Mr. James Lara" << endl;
        cout << "-------------------------------------" << endl;
        break;
    case 5:
        cout << "-------------------------------------" << endl;
        cout << "Reply by Electrician Jake" << endl;
        cout << "I am not Culprit" << endl;
        cout << "Who is Mr. James Lara I dont even know him" << endl;
        cout << "-------------------------------------" << endl;
        break;
    case 6:
        cout << "-------------------------------------" << endl;
        cout << "Reply by Clara the Guest" << endl;
        cout << "He was my Business Partner" << endl;
        cout << "We have a meeting" << endl;
        cout << "But I am not Culprit" << endl;
        cout << "I have not Murdered him" << endl;
        cout << "-------------------------------------" << endl;
        break;
    }
}
void scenario2()
{
    cout << endl;
    cout << "=====================================" << endl
         << endl;
    cout << "     MURDER INVESTIGATION GAME!" << endl;
    cout << endl
         << "=====================================";
    cout << endl;
    cout << "-------------------------------------" << endl;
    cout << "|        GAME INSTRUCTIONS...       |" << endl;
    cout << "-------------------------------------" << endl
         << endl;
    cout << "A Crime has been ocurred in Serena Hotel!" << endl;
    cout << "Someone killed Business Tycon Mr. James Lara" << endl;
    cout << "You are the Detective in Charge of Solving it" << endl;
    cout << "Find clues,question suspects,and catch the culprit" << endl
         << endl;
    cout << "-------------------------------------" << endl;
    cout << "|             SUSPECTS!             |" << endl;
    cout << "-------------------------------------" << endl
         << endl;
    cout << "These are the three suspects" << endl;
    cout << "During the incident" << endl;
    cout << "Sophie(Maid) found the body of Mr. James Lara" << endl;
    cout << "Jake(Electrician) was fixing lights in Hallway" << endl;
    cout << "Clara(Guest) met Mr. James Lara for business meeting" << endl
         << endl;
    cout << "-------------------------------------" << endl;
    if (energytotal < 20)
    {
        cout << "-------------------------------------" << endl;
        cout << "Sorry Detective does not have enough energy" << endl;
        cout << "This Detective is not able to do this investegation" << endl;
        cout << "-------------------------------------" << endl;
        summary(energytotal, score);
    }
    // Culprit is generated as random
    int collectedclues = 0;
    srand(time(0));
    int culprit = 1 + rand() % 3;
    int choice;
    cout << "|  where do you wanna investigate   |" << endl;
    cout << "-------------------------------------" << endl
         << endl;
    while (energytotal > 20)
    {
        if (!visited[1])
            cout << "For Bedroom select(1)" << endl;
        if (!visited[2])
            cout << "For Hallway select(2)" << endl;
        if (!visited[3])
            cout << "For Backyard select(3)" << endl
                 << endl;
        if (!visited[4])
            cout << "Investigation from the Sophie Press(4)" << endl;
        if (!visited[5])
            cout << "Investigation from the Jake Press(5)" << endl;
        if (!visited[6])
            cout << "Investigation from the Clara Press(6)" << endl
                 << endl;
        cout << "Guess Directly the Culprit Press(0)  : ";
        cin >> choice;
        if (choice < 0 || choice > 6)
        {
            cout << "Invalid Input" << endl;
            cout << "Please Select the correct input!" << endl;
            continue;
        }

        if (choice != 0 && visited[choice])
        {
            cout << "You have already investigated this place";
            cout << "Select a different input" << endl;
        }
        if (choice != 0)
        {
            visited[choice] = true;
        }
        if (choice == 1)
        {
            energytotal -= 10;
            collectedclues++;
            clue(choice, score, energytotal, culprit);
        }
        else if (choice == 2 || choice == 3)
        {
            energytotal -= 10;
            collectedclues++;
            clue(choice, score, energytotal, culprit);
        }
        else if (choice == 4 || choice == 5 || choice == 6)
        {
            collectedclues++;
            energytotal -= 15;
            score += 15;
            investigation(choice);
        }

        else if (choice == 0)
        {

            int guess;
            cout << "-------------------------------------" << endl;
            cout << "|          who is Culprit?          |" << endl;
            cout << "-------------------------------------" << endl;
            cout << "1.Sophie\n2.Jake\n3.Clara " << endl;
            cout << "Press (1,2,3)" << endl;
            cin >> guess;
            if (guess == culprit)
            {
                score += 50;
                cout << "-------------------------------------" << endl;
                cout << "Congratulations" << endl;
                cout << "You have guessed it Correct" << endl;
                cout << "You have won the game!" << endl;
                cout << "-------------------------------------" << endl;

                summary(energytotal, score);
            }
            else if (guess != culprit)
            {
                cout << "-------------------------------------" << endl;
                cout << "SORRY! " << endl;
                cout << "You Guessed it Wrong." << endl;
                if (culprit == 1)
                {
                    cout << "Culprit was Sophie the Maid!" << endl;
                }
                else if (culprit == 2)
                {
                    cout << "Culprit was Jake the Electrician!" << endl;
                }
                else if (culprit == 3)
                {
                    cout << "Culprit was Clara the Guest!" << endl;
                }
                cout << "-------------------------------------" << endl;
                summary(energytotal, score);
            }
        }

        cout << "Collected Clues = " << collectedclues << endl;
        cout << "Remaing Energy = " << energytotal << endl;
        cout << "-------------------------------------" << endl;
        continue;
    }
}
void clue(int choice, int reputation, int energy, int culprit)
{
    int initialclue = 0;
    initialclue++;
    cout << endl
         << "-------------------------------------" << endl;
    cout << "Detective started looking for clues" << endl;
    cout << "-------------------------------------" << endl
         << endl;
    energy = energy - 20;

    if (choice == 1)
    {
        int hint;
        srand(time(0));
        hint = 1 + rand() % 3;
        if (hint == 1)
        {
            cout << "You just discovered a mystery Handkrchiff and Syrup" << endl;
            reputation = reputation + 10;
        }
        else if (hint == 2)
        {
            cout << "You discovered Toren invitation card of a meeting" << endl;
            reputation = reputation + 30;
        }
        else if (hint == 3)
        {
            cout << "You discovered an expensive mystery Knife stained with blood" << endl;
            reputation = reputation + 40;
        }
    }
    else if (choice == 2)
    {
        cout << "You discovered nothing" << endl;
        reputation = reputation - 10;
    }
    else if (choice == 3)
    {
        cout << "You discovered Broken Pieces of Wine Glass" << endl;
        reputation = reputation + 20;
    }
    cout << endl
         << "-------------------------------------" << endl;
}
int main()
{

    scenario2();
    _getch();
    return 0;
}
