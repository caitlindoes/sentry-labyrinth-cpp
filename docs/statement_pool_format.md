# Statement Pool Format Standard

Each guild member will have their statements stored as a vector<string>, in this order:

vector<string> <memberName>_statements = {
    "statement 1",
    "statement 2",
    "statement 3"
    // etc
};

All statements must be:

1) In plain English text.
2) Written as a positive direct claim.
3) End with a period.

Example template:

vector<string> Caitlin_statements = {
    "Caitlin won a poetry contest.",
    "Caitlin hates mac and cheese.",
    "Caitlin has a ball python.",
    "Caitlin’s Kia Sorento spontaneously caught on fire."
};

All members must follow this EXACT style → same punctuation + same format.
