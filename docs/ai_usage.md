AI Use Log
ChatGPT (OpenAI)

Context: I turned to ChatGPT when working on Rosalind Problem #9 (GC content). My challenge was figuring out how to identify the FASTA entry with the highest GC percentage.

Prompt: I asked for pseudocode that would track the maximum GC% while looping through multiple sequences.

Response: It suggested keeping two variables (best_id and best_gc) updated during the loop.

My changes: I swapped in my own variable names, added rounding to six decimal places, and inserted extra print statements for debugging.

Verification: I built a small FASTA file with three sequences, hand-calculated their GC%, and confirmed the code highlighted the right record.

Gemini (Google)

Context: I consulted Gemini when writing the nucleotide counting script (A, C, G, T). My first attempt used repetitive if-else statements.

Prompt: I asked for a neater, more “Pythonic” solution.

Response: It recommended using a dictionary and looping over it instead of hardcoding each base.

My changes: I kept the dictionary design but restricted it to just A, C, G, and T so stray characters wouldn’t be included.

Verification: I compared its output with Python’s built-in str.count() for the same DNA string — the counts matched.

DeepSeek (notes only)

Context: I didn’t copy any DeepSeek code into my repo, but I asked it about efficiency concerns.

Prompt: I wanted to know if collections.Counter would be faster than a dictionary loop for large DNA strings.

Response: It suggested Counter might be a bit quicker.

My decision: I stayed with the dictionary because clarity mattered more than micro-optimizations.

Verification: I tested both approaches on a 100k-base random DNA sequence. The runtimes were nearly identical, so my simpler approach was fine.
