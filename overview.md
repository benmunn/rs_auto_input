# ACTIVITY LIST

1. PPMC
2. OEQ
3. PWAC
4. PWM
5. WAC
6. TMC
7. CC
8. SFI
9. WMM

## PPMC 

### Task overview

1. Collect all image files in one directory
2. Rename each image file "[book\_id]\_cover" by scanning the images with OCR, matching the title on the cover to the title listed in the book\_info sheet. 
3. Run LLM analysis of images to pull out descriptions, and place them in "description" column of the "PPMC" sheet in the extraction\_data.xlsx file, in the row corresponding to the title of the book with the matching ID. If the level of the book is "K-R", or "K-S", the description should just be an object, animal, plant, or person in the image. If the level of the book is "1-R" or "1-S", then it should be a description of what is happening, or where the subject is in the form of a sentence. Examples for K-level: "dog", "teacher", "tree", "pencil"; examples for 1-level: "The dog is on the floor.", "The teacher has a book.", "The child plays the piano."
4. Adjust correct descriptions, add 2 distractors per book activity. The k-level ("K-R" and "K-S" in the level column) distractors should also be single words or noun phrases, while the 1-level ("1-R" and "1-S" in the level column) distractors should be sentences. 
5. Double check spelling, level appropriateness, and lack of overlapping answers. All sentences should be understandable by EFL students at a reading level equivalent to a native 1st-grade student. The distractor answers should be reasonable but clearly wrong. For 1-level distractors, the distractor sentences should not share subjects or predicates with the correct answer sentence. 
6. For each book, enter the correct answer and 2 distractor answers in a random order on the excel document columns "text1", "text2", and "text3"; for "answer1", enter "correct" if "text1" is the correct answer and enter "off-topic" if it is one of the distractors. Do the same for "answer2" and "text2", then "answer3" and "text3", indicating whether each answer choice is "correct" or "off-topic" (incorrect). 
7. For each row in the PPMC sheet, copy the value in the "title" column and paste it in the "https://admin.reading-space.com/books" search bar, containing the placeholder text "Search books by title, author, genre, or descriptior". If only one table row (HTML element with "\<tr\>" tag) is present in the table (HTML table "\<table class=w-full border-collapse text-sm\>"), click the element with the "direct hit" emoji (U+1F3AF): "\<button type="button" class="rounded border-none bg-transparent p-1 text-base transition-colors hover:bg-[#dbeafe] disabled:cursor-not-allowed disabled:opacity-50 disabled:hover:bg-transparent"\>U+1F3AF\</button\>" in the same table. If there are more than one rows in that table, look for an exact match for the book title in one of the table cells ("\<td\>" elements) in each table row. If you find a match for the book title within a given table row, look within that table row for the "direct hit" button mentioned above and click it. 
8. On the next page, after the button has been clicked, find the "\<h2\>" header with "Picture Prompt Multiple Choice" as the text contents, then look into the table immediately below it. Click on the "add" (\<a class="btn btn-neutral btn-sm w-24 text-white" href="/activities/2308/picture-prompt-multiple-choice/create"\>+ Add\</a\>) button within the second \<tr\> of the \<tbody\> within the \<table\>. 
9. On the next page
