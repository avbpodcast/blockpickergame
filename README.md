Blockpicker Entropy Game
Blockpicker is an interactive, game-based tool for generating BIP39-compliant 24-word mnemonic seed phrases. Players select blocks on a 12x12 grid in a turn-based game against a computer opponent, contributing entropy to create a cryptographically secure seed phrase. The game combines user interaction with seeded randomness to ensure robust entropy for secure wallet seed generation.
Features
Interactive Gameplay: Players and the computer take turns picking blocks on a 12x12 grid, with a limit of 36 selections (12 by the user, 24 by the computer).

Computer Strategies: Choose from four computer play styles:
Wild: Fully random block selection.

Orderly: Selects blocks in rows or columns systematically.

Follower: Picks blocks near the player's last selection.

Random: Randomly switches between the above styles for each pick.

Blocked Area: After the first user pick, place a 3x3 blocked area to add strategic entropy.

Secure Entropy Generation: Uses SHA-256 hashing with a random 32-byte salt and user-selected block indices to generate a 256-bit entropy seed.

BIP39 Mnemonic: Converts the entropy into a 24-word BIP39-compliant mnemonic seed phrase.

Responsive Design: Mobile-friendly interface with a clean, modern UI.

How It Works
Game Setup:
A 12x12 grid is initialized with 144 blocks.

The user selects a computer play style from the dropdown menu.

A 32-byte random salt is generated for seeded randomness.

Gameplay:
The user starts by picking a block, followed by the computer making two picks based on the selected style.

After the first user pick, the user places a 3x3 blocked area, which restricts further selections.

The game continues with alternating turns (1 user pick, 2 computer picks) until 36 blocks are selected.

Entropy Generation:
The indices of the 36 selected blocks, along with the coordinates of the 3x3 blocked area, are hashed using SHA-256 to produce a 256-bit entropy seed.

Salting and other undisclosed ways of peppering are adding to the randomness and non-replayable randomness

The entropy is displayed as a hexadecimal string.

Mnemonic Generation:
Click the "Get 24 word seed phrase" button to convert the entropy into a BIP39-compliant 24-word mnemonic using the standard wordlist.

The mnemonic is displayed and can be copied for use in cryptocurrency wallets.

Installation
No installation is required! Blockpicker is a single HTML file that runs in any modern web browser with JavaScript enabled.
Just download the index.html file.

Run:
Open index.html in a web browser (e.g., Chrome, Firefox).

Ensure JavaScript is enabled and the browser supports the Web Crypto API for secure random number generation.

Usage
Open the index.html file in your browser.

Select a computer play style from the dropdown menu.

Click any block to start the game, then place the 3x3 blocked area after your first pick.

Continue picking blocks in turn with the computer until 36 blocks are selected.

View the generated 256-bit entropy hash.

Click "Get 24 word seed phrase" to display the BIP39 mnemonic.

Use the "Reset" button to start a new game.

Note: The generated mnemonic is sensitive and should be stored securely. Use it only in trusted environments, and do not share it publicly.
Security Considerations
Entropy Source: Combines user-selected block indices, computer picks (seeded with a random salt), and the blocked area coordinates for robust entropy.

Cryptographic Hashing: Uses SHA-256 via the Web Crypto API for secure entropy generation.

Seeded RNG: A 32-byte random salt ensures reproducible yet unpredictable computer picks.

Client-Side Execution: All operations run locally in the browser, ensuring no sensitive data is transmitted.

Warning: Use the generated seed phrases responsibly. Store them offline and never expose them in untrusted environments.
Dependencies
None! The tool is a standalone HTML file with embedded CSS and JavaScript.

Requires a modern browser with support for the Web Crypto API (window.crypto.subtle).

Contributing
Contributions are welcome! To contribute:
Fork the repository.

Create a feature branch (git checkout -b feature/your-feature).

Commit your changes (git commit -m "Add your feature").

Push to the branch (git push origin feature/your-feature).

Open a pull request.

Please ensure code follows the existing style and includes appropriate tests.
License
This project is licensed under the MIT License (LICENSE).
Support
Home: allesvoorbitcoin.be

Contact: Nostr Profile

Tip Jar: Donate

Version: 1.2
Author: [Your Name or Organization]
Repository: [Replace with your GitHub repository URL]

