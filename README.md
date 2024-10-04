# flowlogs

# Flow Log Parser

This project parses flow log data and maps each entry to a tag based on a lookup table. The output is a summary file showing the counts of matches for each tag and each port/protocol combination.

#Assumptions

- The program only supports the default flow log format (version 2).
- Input flow logs should follow the format provided in `flow_logs.txt`.
- A CSV file (`lookup_table.csv`) containing port, protocol, and tag mappings is required.
- The matching process is case-insensitive.

# Requirements

- Python 3.x is required.
- No additional libraries are necessary, ensuring the program can be run locally without installing extra packages.

#Instructions to Run the Program

1. Clone the repository:
   
   git clone https://github.com/your_username/Flow_Log_Parser.git
   cd Flow_Log_Parser
   
2. Run the Program: Execute the Python script:
    
    python mapping.py
    
    The script will read flow_logs.txt and lookup_table.csv, process the data, and generate an output file (output.txt) with   summarized information.

3. Output File: The results will be saved in output.txt, which will include:

        Tag Counts: The number of flow log entries matching each tag.
        Port/Protocol Combination Counts: The number of matches for each port/protocol pair.
        
4.Testing
    flow_logs.txt: A sample file containing flow logs for testing. Modify this file to test different scenarios.
    
    lookup_table.csv: Contains 1200 randomly generated port/protocol/tag mappings.

The script has been tested with various sample logs, and it correctly outputs the number of matches per tag and port/protocol.

5. Code Explanation
The mapping.py script processes flow logs by:

Reading the lookup_table.csv to build a dictionary of mappings.

Parsing the flow_logs.txt file and mapping each entry to a tag based on the destination port and protocol.

Counting how many times each tag and port/protocol combination occurs.

The results are then written to output.txt.

6. Analysis

The program processes the flow logs efficiently by utilizing Python’s built-in libraries without external dependencies.
The output format is designed to be easy to read and analyze, with tag and port/protocol summary counts provided.

