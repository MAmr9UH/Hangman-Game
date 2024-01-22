#include <vector>
#include <cstdlib>  // For rand() and srand() functions
#include <ctime>    // For time() function

using namespace std;
// Function to display the hangman figure based on the number of incorrect guesses
void displayHangman(int incorrectGuesses) {
    switch (incorrectGuesses) {
        case 0:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 1:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 2:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 3:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "  /|   |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 4:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "  /|\\  |" << std::endl;
            std::cout << "       |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 5:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "  /|\\  |" << std::endl;
            std::cout << "  /    |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
        case 6:
            std::cout << "   +---+" << std::endl;
            std::cout << "   |   |" << std::endl;
            std::cout << "   O   |" << std::endl;
            std::cout << "  /|\\  |" << std::endl;
            std::cout << "  / \\  |" << std::endl;
            std::cout << "       |" << std::endl;
            break;
    }
}


int main(){

srand(static_cast<unsigned int >(time(nullptr))); //set random seed
  vector<string>words={"bannana", "apple", "orange", "grape","Hangout", "finger", "sister", "brother", "friend", "family", "school", "teacher", "student", "library"};

string word=words[rand()%words.size()]; //SET WORD TO A RANDOM WORD IN THE VECTOR

  string word_guessed(word.length(),'_');//this line to store the guessed word with underscores
int incorrectGuesses=0; //this line to store the number of incorrect guesses
  string guessed_chars="";

  cout<<"Welcome To Hangman"<<endl;
  

do{  displayHangman(incorrectGuesses);

   cout<<"word: "<<word_guessed<<endl;
   
   cout<< "Guessed characters: "<<guessed_chars<<endl;
char guess;
    cin>>guess;

   if(guessed_chars.find(guess)!=string::npos){
cout<<"You already guessed that character"<<endl;
continue;
   }
guessed_chars=guessed_chars+guess;

   bool Theguess =false;
   for(int i=0;i<word.length();i++){  

     if(word[i]==guess){
       word_guessed[i]=guess;
       Theguess=true;
     }
     }
if(!Theguess){
  cout<<"Incorrect guess"<<endl;
  incorrectGuesses++;
}
   

if(word_guessed==word){

  cout<<"Congratulations! You guessed the word: "<<word<<endl;
  break;
}
 
if(incorrectGuesses==6){
displayHangman(incorrectGuesses);
cout<< "You lost! The word was: "<<word<<endl;
  break;
}
  } while (true);


  
}
