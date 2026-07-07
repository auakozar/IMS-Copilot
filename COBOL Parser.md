How to recognize divisions, sections, paragraphs, CALL statements SQL, DL/I calls, COPY statements, and datata defonitions

    Purpose
        What is the parser trying to accomplish?
    Input
        COBOL source files
        Copybooks
        Embedded SQL
        DL/I calls
    Output
        A structured representation (Abstract Syntax Tree or equivalent)
        List of paragraphs
        Data items
        CALL statements
        COPY statements
        DL/I calls (GU, GN, REPL, ISRT, DLET, etc.)
        File references
        Database references
    Parser Phases
        Lexical analysis
        Syntax analysis
        Semantic analysis
        Symbol table construction
    IMS-Specific Logic
        Detect PCB usage
        Identify SSA construction
        Recognize database access patterns
        Track segment usage
        Determine whether a program reads, updates, inserts, or deletes data
    Output Format
        JSON
        Graph nodes
        Relationships for the knowledge graph
    Error Handling
        Invalid COBOL
        Missing copybooks
        Unsupported compiler directives
    Testing
        Sample COBOL programs
        Expected parser output
        Regression tests

T    Purpose
        What is the parser trying to accomplish?
    Input
        COBOL source files
        Copybooks
        Embedded SQL
        DL/I calls
    Output
        A structured representation (Abstract Syntax Tree or equivalent)
        List of paragraphs
        Data items
        CALL statements
        COPY statements
        DL/I calls (GU, GN, REPL, ISRT, DLET, etc.)
        File references
        Database references
    Parser Phases
        Lexical analysis
        Syntax analysis
        Semantic analysis
        Symbol table construction
    IMS-Specific Logic
        Detect PCB usage
        Identify SSA construction
        Recognize database access patterns
        Track segment usage
        Determine whether a program reads, updates, inserts, or deletes data
    Output Format
        JSON
        Graph nodes
        Relationships for the knowledge graph
    Error Handling
        Invalid COBOL
        Missing copybooks
        Unsupported compiler directives
    Testing
        Sample COBOL programs
        Expected parser output
        Regression tests

The parser to answer business questions. 
For example:
Which programs update the CUSTOMER segment?
Where is field ACCT-BALANCE referenced?
What applications call transaction PAY1?
What programs perform REPL operations on POLICY?
If this DBD changes, what is the impact?

