Day-9
# Secret Auction 🏆

Welcome to the **Secret Auction** project! This Python application simulates a fun and interactive secret bidding process, allowing multiple users to compete for an auction without knowing others' bids until the winner is announced.

---

## Project Description

The **Secret Auction** application allows users to input their bids in secrecy. Once all participants have entered their bids, the program determines and displays the winner with the highest bid.

---

## Features

- **Secret Bidding**: Keeps bids private until the auction concludes.
- **Dynamic User Input**: Allows multiple users to participate by continuously taking input.
- **Clear Display**: Uses ASCII art for an enhanced visual experience.
- **Cross-platform Clear Screen**: Clears the console after each bid (for platforms supporting the `os` library).

---

## How It Works

1. Each participant enters their name and bid amount.
2. Participants are prompted to specify if there are more bidders:
   - If `yes`, the screen clears, and the program continues collecting bids.
   - If `no`, the bidding ends, and the winner is announced.
3. The program compares all bids and declares the winner with the highest bid.

---

## ASCII Art

The project displays a visually appealing auction-themed logo:

```
                         ___________
                         \         /
                          )_______(
                          |"""""""|_.-._,.---------.,_.-._
                          |       | | |               | | ''-.
                          |       |_| |_             _| |_..-'
                          |_______| '-' `'---------'` '-'
                          )"""""""(
                         /_________\
                       .-------------.
                      /_______________\
```

---

## Prerequisites

- Python 3.x installed on your system.
- **Optional**: The `os` library is required for the screen-clearing functionality.

---

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aditya-kr86/Secret-Auction.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd Secret-Auction
   ```

3. **Run the program**:
   ```bash
   python secret_auction.py
   ```

---

## Example Usage

```
What is your name?: Alice
What is your bid?: ₹500
Are there any other bidders? Type 'yes' or 'no'.
yes

What is your name?: Bob
What is your bid?: ₹700
Are there any other bidders? Type 'yes' or 'no'.
no

The winner is Bob with a bid of ₹700
```

---

## Code Overview

### Key Components

1. **User Input**:
   - Accepts names and bid amounts.
   - Asks if additional participants want to join.
2. **Bid Processing**:
   - Stores bids in a dictionary with names as keys and bid amounts as values.
   - Determines the highest bid and the winner.
3. **Clear Console**:
   - Uses `os.system('cls')` (Windows) or `os.system('clear')` (Unix/Linux/MacOS) to clear the screen between bids.

### Main Functionality

```python
def find_highest_bidder(bidding_record):
    highest_bid = 0
    winner = ""
    for bidder in bidding_record:
        bid_amount = bidding_record[bidder]
        if bid_amount > highest_bid: 
            highest_bid = bid_amount
            winner = bidder
    os.system('cls')
    print(logo)
    print(f"The winner is {winner} with a bid of ₹{highest_bid}")
```

---

## Project Structure

```
Secret-Auction/
├── secret_auction.py  # Main script for the auction
├── art.py             # Contains the ASCII art logo
├── README.md          # Project documentation
```

---

## Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests for improvements or new features.

---

## Author

- **Aditya Kumar**  
  [GitHub Profile](https://github.com/aditya-kr86)  
  [Email](mailto:adityakumargupta082003@gmail.com)

---

## License

This project is open-source and licensed under the MIT License.

--- 

## Feedback

If you have any suggestions or feedback, feel free to reach out to me via email or GitHub.

Happy Bidding! 🤑
