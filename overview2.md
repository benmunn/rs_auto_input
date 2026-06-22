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

### Image Collection

1. Collect all image files in one directory, then name the directory "ppmc\_img"
2. create a list of all of the filenames in the "ppmc\img" directory.
3. For each image, rename each image file "[book\_id]\_cover" by scanning the images with OCR, matching the title on the cover to the title listed in the book\_info sheet.
4. Rename each image file "[book\_id]\_cover" 
  
### 

3. Run LLM analysis of images to pull out descriptions, and place them in "description" column of the "PPMC" sheet in the extraction\_data.xlsx file, in the row corresponding to the title of the book with the matching ID. If the level of the book is "K-R", or "K-S", the description should just be an object, animal, plant, or person in the image. If the level of the book is "1-R" or "1-S", then it should be a description of what is happening, or where the subject is in the form of a sentence. Examples for K-level: "dog", "teacher", "tree", "pencil"; examples for 1-level: "The dog is on the floor.", "The teacher has a book.", "The child plays the piano."

4. Adjust correct descriptions, add 2 distractors per book activity. The k-level ("K-R" and "K-S" in the level column) distractors should also be single words or noun phrases, while the 1-level ("1-R" and "1-S" in the level column) distractors should be sentences. 
5. Double check spelling, level appropriateness, and lack of overlapping answers. All sentences should be understandable by EFL students at a reading level equivalent to a native 1st-grade student. The distractor answers should be reasonable but clearly wrong. For 1-level distractors, the distractor sentences should not share subjects or predicates with the correct answer sentence. 
6. For each book, enter the correct answer and 2 distractor answers in a random order on the excel document columns "text1", "text2", and "text3"; for "answer1", enter "correct" if "text1" is the correct answer and enter "off-topic" if it is one of the distractors. Do the same for "answer2" and "text2", then "answer3" and "text3", indicating whether each answer choice is "correct" or "off-topic" (incorrect). 
7. For each book, navigate to "https://admin.reading-space.com/activities/[book\_id]/picture-multiple-choice/create", where "book\_id" is the value in the "book\_id" column of the PPMC sheet
8. Next, click the button "\<button type="button" class="btn w-fit"\>Upload file (png, jpg)\</button\>", then select the file with from "PATHTO/ppmc-img" with the filename in the "image\_file" column of the PPMC sheet. With the file selected, press ENTER or click the "open" button on the file explorer UI. 
9. Find the \<label\> tagged element containing a \<span\> element with the text "Question text", then select the \<textarea\> tagged element within the same \<label\> element as the \<span\>, which should be "\<textarea class="form-input min-h-[80px] rounded border border-neutral-200 px-3 py-2" placeholder="What do you see in this picture?"\>\</textarea\>" . With this text area selected, enter the value in the cell in the "question" column of the "PPMC" sheet in the row of the relevant book. 
10. Find the button "\<button type="button" class="btn btn-neutral btn-sm text-white"\>+ Add Answer\</button\>". Click this button twice to add two answers. 
11. Under the <h2 class="text-xl font-semibold text-gray-900">Answers</h2> heading, there will be 3 div classes like this: "<div class="flex flex-col gap-4 rounded-lg bg-white p-6 shadow-md"><div class="flex items-center justify-between"><h3 class="text-base font-semibold text-gray-900">Answer <!-- -->[answer_number]</h3></div><label class="flex flex-col gap-2"><span class="text-sm font-semibold text-gray-700">Answer text</span><input type="text" class="form-input rounded border border-neutral-200 px-3 py-2" value=""></label><label class="flex flex-col gap-2"><span class="text-sm font-semibold text-gray-700">Answer type</span><select class="form-input rounded border border-neutral-200 px-3 py-2"><option value="correct">Correct</option><option value="offTopic" selected="">Off topic</option><option value="closestAnswer">Closest answer</option></select></label></div>" where [answer\_number] is "1", "2", or "3". For each of these 3 div elements, with [answer\_number] equal to "1", "2", or "3" repeat the following process:
a. Copy the value in the "text[answer\_number]" column of the "PPMC" sheet, then paste it in the input field of the element "<label class="flex flex-col gap-2"><span class="text-sm font-semibold text-gray-700">Answer text</span><input type="text" class="form-input rounded border border-neutral-200 px-3 py-2" value=""></label>".Then, within the "<select class="form-input rounded border border-neutral-200 px-3 py-2"><option value="correct">Correct</option><option value="offTopic" selected="">Off topic</option><option value="closestAnswer">Closest answer</option></select>" element in the same div, select the <option value="correct"> element if "answer[answer\_number]"="correct" in the PPMC sheet, or select the <option value="offTopic"> if "answer[answer\_number]"="off-topic" in the PPMC sheet. 
12. Click the button "<button type="button" class="bg-button-neutral btn text-white">💾 Create</button>" 
