#include <iostream>
#include <vector>
#include <string>

using namespace std;

struct Question {
    string prompt;
    vector<string> choices;
    char correctAnswer;
};

void askQuestion(const Question& q, int& score, int questionNumber) {
    cout << "\nQuestion " << questionNumber << ": " << q.prompt << "\n";
    for (size_t i = 0; i < q.choices.size(); ++i) {
        cout << static_cast<char>('A' + i) << ") " << q.choices[i] << "\n";
    }

    char answer;
    cout << "Your answer (A/B/C/D): ";
    cin >> answer;
    answer = toupper(answer);

    if (answer == q.correctAnswer) {
        cout << "✅ Correct!\n";
        score++;
    } else {
        cout << "❌ Wrong. The correct answer was " << q.correctAnswer << ".\n";
    }
}

int main() {
    vector<Question> quiz = {
        {"What is the capital of France?", {"Paris", "London", "Rome", "Berlin"}, 'A'},
        {"Which planet is known as the Red Planet?", {"Earth", "Venus", "Mars", "Jupiter"}, 'C'},
        {"What is 9 + 10?", {"19", "21", "20", "18"}, 'A'},
        {"Who wrote 'Romeo and Juliet'?", {"Mark Twain", "Shakespeare", "Hemingway", "Dickens"}, 'B'},
        {"Which gas do plants absorb?", {"Oxygen", "Nitrogen", "Carbon Dioxide", "Hydrogen"}, 'C'},
        {"How many continents are there?", {"5", "6", "7", "8"}, 'C'},
        {"What is the boiling point of water?", {"90°C", "100°C", "110°C", "80°C"}, 'B'},
        {"Which animal is known as the King of the Jungle?", {"Elephant", "Tiger", "Lion", "Panther"}, 'C'},
        {"What is the largest ocean?", {"Atlantic", "Indian", "Arctic", "Pacific"}, 'D'},
        {"What is the chemical symbol for gold?", {"Au", "Ag", "Go", "Gd"}, 'A'}
    };

    cout << "=============================\n";
    cout << "      QUIZ GAME     \n";
    cout << "=============================\n";
    cout << "Answer all 10 questions correctly to win!\n";

    int score = 0;

    for (size_t i = 0; i < quiz.size(); ++i) {
        askQuestion(quiz[i], score, static_cast<int>(i + 1));
    }

    cout << "\n=============================\n";
    if (score == 10) {
        cout << "🎉 Congratulations! You answered all questions correctly!\n";
        cout << "🏆 YOU WIN!\n";
    } else {
        cout << "😢 You answered " << score << " out of 10 correctly.\n";
        cout << "Better luck next time!\n";
    }

    cout << "=============================\n";
    return 0;
}
