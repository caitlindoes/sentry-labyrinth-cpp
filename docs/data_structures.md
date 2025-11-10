# Data Structure Design Options

We are evaluating 3 possible approaches for storing guild members + statements + truth/lie role.

## Option A — Parallel Vectors (simplest C++ beginner friendly)
- `vector<string> memberNames`
- `vector<vector<string>> memberStatements`
- `vector<bool> sentryTruthRole` (true = truthful / false = liar)

Pros:
- Easy for beginners
- Straightforward indexing
Cons:
- Many vectors must stay same index alignment manually

## Option B — Struct Based (intermediate C++ best practice)
struct Sentry {
    string name;
    vector<string> statements;
    bool isTruth;
};
vector<Sentry> sentries;
Pros:
- Cleanest conceptual mapping to real objects
- Easy to expand (scores per member later, etc)
Cons:
- Slightly more advanced, but still beginner friendly

## Option C — File I/O external JSON-ish text data (scalable)
- store members + statements in external text file
- game loads them from file at runtime

Pros:
- scalable, can add statements without recompiling
Cons:
- requires parsing + more code complexity

---


Cait determined Option A is best due to time constraints.
