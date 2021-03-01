//Section 1 (Lines 1-8)
#include <iostream>

#include <vector>

#include <string>

using namespace std;


//Section 2 (Lines 12-25)
int main() {



        //Part I:  Gather Sentence Statistics using Vectors
        int char_count = 0;
        int word_count = 0;
        int word_length = 0;
        int max_length = 0;
        int index = 0;

        vector<char> passage;
        char current ;
        
        

      //Section 3 (Lines 29-65)
        cout << "Please enter all your sentences below(hit enter when finished): " << endl;
       //Sub Section 3.1(Lines 31-33)
        while (cin.get(current))
        {
            passage.push_back(current);
            // Sub Section 3.2(Lines 35-38)
            switch (passage[index])
            {
            case'.':case'!':case' ':case'?': case '-':
            case';':case',':case':':case'\n':
                //Sub Section 3.3 (Lines 40-49)
                if (word_length != 0)
                {
                    ++word_count;
                    if (word_length > max_length)

                        max_length = word_length;






                    word_length = 0;

                    break;
                }
            default:

                ++char_count;
                ++word_length;

                break;

            }
            ++index;
        }

        //Section 4(lines 68-70)
        cout << "Number of words: " << word_count << endl;
        cout << "Average word length: " << (char_count / word_count) << endl;
        cout << "Maximum word length: " << max_length << endl;
        

}
