1. How big is the dataset?
    [ls -lh] (within directory) shows the file size to be 4.7M
    [wc clean_dialog.csv] shows there to be 36860 lines, 670166 words, and 4870970 characters

2. What’s the structure of the data? (i.e., what are the field and what are values in them)
    [head clean_dialog.csv] returns headings "title","writer","pony","dialog"
    for example, in the first ten lines that are returned, the values in these fields show the episode title ("Friendship is Magic, part 1"), writer ("Lauren Faust"), the speaker/pony (in the first couple of lines this is the Narrator), and the script for what was said.

3. How many episodes does it cover?
    [csvtool namedcol title clean_dialog.csv | uniq -c | wc -l] returned 198 episodes

4. During the exploration phase, find at least one aspect of the dataset that is unexpected – meaning that it seems like it could create issues for later analysis.
    One aspect of the dataset that was potentially unexpected was the inclusion of the "Narrator" in the field for "pony." Since the narrator is not actually a character, this could be confusing having this included in the pony column. This is also the case for the inclusion of Spike, a dragon.
    