#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Initialize random seed
    std::srand(std::time(0));

    // Generate a random number between 1 and 100
    int number_to_guess = std::rand() % 100 + 1;
    int guess = 0;

    std::cout << "Welcome to 'Guess the Number'!" << std::endl;
    std::cout << "I've selected a number between 1 and 100. Can you guess it?" << std::endl;

    // Loop until the user guesses the correct number
    while (guess != number_to_guess) {
        std::cout << "Enter your guess: ";
        std::cin >> guess;

        if (guess < number_to_guess) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (guess > number_to_guess) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You've guessed the correct number." << std::endl;
        }
    }

    return 0;
}
