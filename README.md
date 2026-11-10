# project-1-sequence-analysis

**Title and Purpose**

This project uses Python in Google colab to analyse DNA sequencing reads and compare mutations between treated and untreated samples. The overall aim is to investigate whether treatment is associated with increased mutations at specific DNA positions.

**How to Run the Program**

To open and run this program, open notebooks/C7147_Project_1_assessment.ipynb and click "open in colab" at the beginning. Running the code cells in order should result in the final analysis computing at the end of the file.

**Inputs and Outputs**

The program was given with a 200 nucleotide reference sequence, a csv file containing 6,000 sequencing reads, and setup code that is read by python as dictionaries. This setup code includes statistical analysis necessary for the final analysis.

The code checks whether reads are valid and if there are any differences between the reference sequence. It then produces a few tables which include valid and invalid reads, mutation percentages, substitution counts, and the three most frequently mutated positions for each individual sample. It then compares the treatment and control groups using the inputted Welch's t-test code.

**Code Design**

I decided to keep the invalid reads in the analysis because errors should not be ignored in the reporting of results. However, the way that I was able to display the invalid reads did not contribute to the mutation percentages, which would have incorrectly skewed the results. I also decided to sort the mismatch positions by frequency so the three most common mutations could be more easily identified. This would allow the most frequent positions to be easily compared between the treatment and control groups in the final analysis.

**Testing**

Three tests that I ran to check the correctness of the code included my initial test of the validate_read() function. Here I tested five different alternatives to the data to ensure there would be no invalid reads that would be marked as valid. I also tested the find_mutations() function using three tests that would test what the code would output if no mutations, one mutation, and multiple mutations were found. Finally, I tested the statistical analysis in step 5, allowing me to quickly identify if any incorrect outputs were given, rather than waiting for a potential error in the final analysis section. 
