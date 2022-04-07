#include <iostream>
#include <string>
#include <vector>
#include <utility>
#include <set>


std::vector<std::pair<char, size_t>> get_frequency(const std::string &str);


int main(){
    std::string cipher_text{};
    std::cout << "Input a string : ";
    std::getline(std::cin, cipher_text);

    std::vector<std::pair<char,size_t>> frequency{get_frequency(cipher_text)};
    
    for(const auto &i : frequency){
        std::cout << i.first << " appeared " << i.second << " times." << std::endl;
    }

    return 0;
}


std::vector<std::pair<char, size_t>> get_frequency(const std::string &str){
    std::vector<std::pair<char,size_t>> frequency_output{};
    std::set<char> char_buff{};

    for(const char &i : str){
        if(i == ' ')continue;
        char_buff.insert(i);
    }
    
    for(const char &j : char_buff){
        int buff{0};
        for(const char &k : str){
            if(j == k){
                buff++;
            }
        }

        frequency_output.push_back(std::pair(j, buff));
    }
    
    return frequency_output;
}
