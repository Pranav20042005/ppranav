// This array will hold information about all minted NFTs let mintedNftCollection = [];

// This function creates a new NFT object with the provided player data // and adds it to the collection function mintNft(playerName, team, role, battingAvg, bowlingAvg) { const newNftData = { playerName, team, role, battingAvg, // Abbreviation for Batting Average bowlingAvg, // Abbreviation for Bowling Average (if applicable) };

mintedNftCollection.push(newNftData); console.log(Minted new NFT for player: ${playerName} from ${team}); }

// This function iterates through the NFT collection and prints details // of each player NFT function listNfts() { console.log("\n** Listing all minted world cup NFTs **\n"); mintedNftCollection.forEach((playerNft) => { console.log(* Player Name: ${playerNft.playerName}); console.log(* Team: ${playerNft.team}); console.log(* Role: ${playerNft.role}); console.log(* Batting Average: ${playerNft.battingAvg}); if (playerNft.bowlingAvg) { // Print bowling average only if it exists console.log(* Bowling Average: ${playerNft.bowlingAvg}); } console.log("\n"); }); }

// This function returns the total number of minted NFTs function getTotalNfts() { return mintedNftCollection.length; }

// Mint some sample NFTs (function calls can be adjusted as needed) mintNft("Patrick", "Australia", "Batsman", 38.16, null); mintNft("MM Doni", "Zimbawe", "Wicketkeeper-Batsman", 40.25, null); mintNft("Rohit Abdul", "Pakistan", "Batsman", 32.45, null); mintNft("Chris", "New Zealand", "Bowler", 12.34, 24.62); mintNft("Andre Russell", "West Indies", "All-Rounder", 29.14, 27.33); mintNft("David Warner", "Iran Champions", "Batsman", 42.22, null);

listNfts();

const totalMintedNfts = getTotalNfts(); console.log(Total Minted NFTs: ${totalMintedNfts});
