# The Triple Treat

I made a dictionary. You're welcome.

Dictionary Building Process

#### Word Sources

I pulled data from three sources as I wanted to change things up. A standard dictionary, Urban dictionary, a list of IKEA names, and the top 1,000 current brands.

**1. Standard Dictionary**
- **Source**: Public domain English word list
- **Original size**: 370,105 words
- **Processing**: Filtered to keep only words 11+ characters long
- **Result**: 84,103 substantial words
- **Quality**: Traditional English vocabulary, academic terms, technical words

**2. Urban Dictionary**
- **Source**: Urban Dictionary dataset (1999-2016)
- **Original size**: 765,772 entries (1.9GB JSON file)
- **Processing**:
  - Extracted unique words from JSON entries
  - Filtered to 3-20 character words
  - Removed duplicates
  - Further filtered to 11+ character words
- **Result**: 77,698 modern slang words
- **Quality**: Contemporary internet slang, memes, modern vocabulary

**3. IKEA Product Names**
- **Source**: IKEA product naming database
- **Original size**: 1,385 product entries
- **Processing**:
  - Extracted product names from metadata
  - Removed special characters and descriptions
  - Converted to lowercase
  - Filtered to 3-20 character names
- **Result**: 1,360 unique product names
- **Quality**: Swedish/Scandinavian names, international place names, distinctive vocabulary

**4. Brand Names**
- **Source**: I got a GPT to pull the list.

#### Processing
All scripts are located in the `lib/` directory:

**Standard Dictionary Processing:**
# Filter to keep only 11+ character words

**Urban Dictionary Processing:**
# Extract words from 1.9GB JSON dataset
# Input: data/words.json (2,606,521 entries)
# Output: data/urban_words.txt (765,772 words)
# Processing: JSON parsing, duplicate removal, length filtering
# Filter to keep only 11+ character words
# Input: data/urban_words.txt (765,772 words)
# Output: data/urban_words_filtered.txt (77,698 words)
# Removes: 688,074 short words (89.9% reduction)

**IKEA Names Processing:**
# Extract product names from metadata
# Input: data/ikea.txt (1,385 entries)
# Output: data/ikea_names.txt (1,360 words)
# Processing: Regex extraction, special character removal

#### Final Dictionary
- **Combined file**: `data/words.txt` (2.3MB)
- **Total words**: 160,287 unique words
- **Word quality**: 99.2% are 11+ characters long
- **Vocabulary mix**: Traditional, modern slang, and international names

#### Word Distribution
- **12-13 chars**: 62.6% (most common)
- **14-16 chars**: 29.8% (substantial words)
- **17+ chars**: 6.8% (very long words)
- **Short words**: 0.8% (3-10 chars)

This creates a diverse vocabulary perfect for generating interesting, memorable passwords with substantial word lengths.

#### Data Source Characteristics

**Standard Dictionary**:
- **Vocabulary**: Academic, technical, literary, scientific terms
- **Examples**: "abalienating", "abarticulation", "dichlorodiphenyltrichloroethane"
- **Length**: Primarily 12-20+ characters
- **Style**: Formal, sophisticated vocabulary

**Urban Dictionary**:
- **Vocabulary**: Internet slang, memes, contemporary culture
- **Examples**: "scamazonning", "myfriendpassedout", "aaaaaaaaaaaa"
- **Length**: Varied, includes many 12-15 character words
- **Style**: Modern, edgy, internet culture

**IKEA Product Names**:
- **Vocabulary**: Swedish names, place names, international terms
- **Examples**: "absorb", "alarm", "alkalisk", "allamåla"
- **Length**: 3-12 characters (shorter, memorable names)
- **Style**: International, distinctive, memorable

**Combined Result**:
- **Total diversity**: 160,287 unique words
- **Vocabulary mix**: Traditional + Modern + International
- **Password quality**: Substantial, memorable, varied
- **Art potential**: Rich source material for creative prompts

Have fun.
