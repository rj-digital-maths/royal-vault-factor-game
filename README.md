================================================================================
                    THE ROYAL VAULT - FACTORIZATION GAME
================================================================================

A gamified mathematics web application designed to build fluency 
in factor identification, divisibility rules, and factor-pair completeness 
for numbers 1 through 100.

================================================================================
                    THE ROYAL VAULT - FACTORIZATION GAME
================================================================================

A gamified middle-school mathematics web application designed to build fluency 
in factor identification, divisibility rules, and factor-pair completeness 
for numbers 1 through 100.

Designed for Class 6 & Class 7 curriculum frameworks (CBSE / NEP 2020 / Ganit 
Prakash alignment) and interactive classroom whiteboards, tablets, or desktops.

--------------------------------------------------------------------------------
1. PACKAGE CONTENTS
--------------------------------------------------------------------------------

- royal_vault_trial.html : Free Trial / Demo edition with strict persistent limits.
- royal_vault_full.html  : Full Royal Edition with unrestricted access and tools.
- README.txt             : Architecture guide, rules, and deployment instructions.


--------------------------------------------------------------------------------
2. EDITION SPECIFICATIONS
--------------------------------------------------------------------------------

[A] TRIAL EDITION (royal_vault_trial.html)
------------------------------------------
- Designed for marketing, lead generation, or evaluation demos.
- Fixed 5-vault trials per difficulty tier:
    * Easy Tier: 5 curated puzzles (2 to 4 factors).
    * Moderate Tier: 5 curated puzzles (5 to 8 factors).
    * Difficult Tier: 5 curated puzzles (9 to 12 factors).
- Persistent Anti-Tamper System:
    * Uses browser localStorage ('royal_vault_strict_trial_v1').
    * Page refresh (F5), tab closing, or back-navigation CANNOT bypass or reset
      the trial counter once completed.
- Hard Paywall Gate:
    * Automatically triggers upon completing the 5th chamber.
    * Greys out and locks the canvas behind an unclosable royal modal.
    * Features a direct call-to-action button to purchase the Full Royal Edition.

[B] FULL ROYAL EDITION (royal_vault_full.html)
---------------------------------------------
- Commercial / full classroom edition with no limits or paywalls.
- Dynamic Tier Modes:
    * Easy (2 to 4 factors)
    * Moderate (5 to 8 factors)
    * Difficult (9 to 12 factors)
    * Full 1-100 Matrix (direct manual dropdown showing factor counts).
- Pedagogical Features:
    * Live Factor-Pair HUD: Automatically matches and displays complementary 
      pairs (e.g., 4 x 9 = 36, 6 x 6 = 36) as keys are locked in.
    * Random Target Generator: Instantly shuffles and serves new challenges.
    * Continuous Auto-Progression: Automatically unlocks and loads the next 
      number when all sockets are filled.


--------------------------------------------------------------------------------
3. CORE GAME MECHANICS & MATHEMATICAL RULES
--------------------------------------------------------------------------------

- Central Safe Dial:
    * Displays the target number N in the center hub.
    * Radial socket keyholes generate dynamically based on the exact factor 
      count d(N) of the active target (ranging from 2 up to 12 slots).

- Dual Key Racks:
    * Left-Hand Side (LHS): Keys 1 to 50 arranged in a 5-column x 10-row matrix.
    * Right-Hand Side (RHS): Keys 51 to 100 arranged in a 5-column x 10-row matrix.

- Input & Validation Rules:
    1. Upper Bound Rule: Keys strictly greater than the target number (k > N) 
       are dimmed and cannot be picked, demonstrating that all factors of N 
       must be <= N.
    2. Click-to-Slot Interaction: Tap a key on either rack, then click any 
       open perimeter keyhole socket to insert it.
    3. Error Penalty: Choosing a non-divisor registers a mechanical strike. 
       Accumulating 3 strikes jams the vault mechanism and resets active sockets.
    4. Victory State: Inserting all distinct factors unlocks the vault with a 
       mechanical fanfare and rotates the central dial.


--------------------------------------------------------------------------------
4. HOW TO HOST ON GITHUB PAGES (FREE & LIVE IN 30 SECONDS)
--------------------------------------------------------------------------------

Step 1: Create a new repository on GitHub (e.g., 'royal-vault-game').
Step 2: Upload both HTML files directly to the root of the repository.
Step 3: (Optional) If you want the Trial edition to load by default as the main
        website, rename 'royal_vault_trial.html' to 'index.html'.
Step 4: Go to Repository "Settings" -> Click "Pages" on the left menu.
Step 5: Under "Build and deployment", set Source to "Deploy from a branch", 
        choose 'main' (or 'master') as the branch, and click "Save".
Step 6: GitHub will generate your live URL:
        https://<your-username>.github.io/royal-vault-game/


--------------------------------------------------------------------------------
5. CUSTOMIZATION INSTRUCTIONS
--------------------------------------------------------------------------------

- Changing Purchase Link (Trial Version):
  Open 'royal_vault_trial.html' in any text editor, locate line ~340:
      window.open('https://your-purchase-link.com', '_blank')
  Replace 'https://your-purchase-link.com' with your actual Gumroad, Stripe, 
  website, or payment checkout link.

- Resetting LocalStorage During Development Testing:
  To test the trial lock reset in your own browser:
  Open Developer Tools (F12) -> Console -> run:
      localStorage.removeItem("royal_vault_strict_trial_v1");
  Then refresh the page.

================================================================================

(c) 2026 RJ Digital Interactive Maths. All Rights Reserved.
Concept & Pedagogical Design.
