Download Link: https://assignmentchef.com/product/solved-csc-355-database-systems-401-410-assignment-2
<br>
<table class="highlight tab-size js-file-line-container" data-tab-size="8">

 <tbody>

  <tr>

   <td id="L2" class="blob-num js-line-number" data-line-number="2"></td>

   <td id="LC2" class="blob-code blob-code-inner js-file-line">Assignment 2</td>

  </tr>

  <tr>

   <td id="L3" class="blob-num js-line-number" data-line-number="3"></td>

   <td id="LC3" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L6" class="blob-num js-line-number" data-line-number="6"></td>

   <td id="LC6" class="blob-code blob-code-inner js-file-line">Reading: The posted Lecture 3 and Lecture 4 Slides, and Ullman/Widom Sections 2.3, 6.5, 7.1-7.3, and 6.1. [Next week: Ullman/Widom Sections 6.2-6.4.]</td>

  </tr>

  <tr>

   <td id="L7" class="blob-num js-line-number" data-line-number="7"></td>

   <td id="LC7" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L8" class="blob-num js-line-number" data-line-number="8"></td>

   <td id="LC8" class="blob-code blob-code-inner js-file-line">Your task in this assignment is to write a script to create a small database (three linked tables).</td>

  </tr>

  <tr>

   <td id="L9" class="blob-num js-line-number" data-line-number="9"></td>

   <td id="LC9" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L10" class="blob-num js-line-number" data-line-number="10"></td>

   <td id="LC10" class="blob-code blob-code-inner js-file-line">Steps:</td>

  </tr>

  <tr>

   <td id="L11" class="blob-num js-line-number" data-line-number="11"></td>

   <td id="LC11" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L12" class="blob-num js-line-number" data-line-number="12"></td>

   <td id="LC12" class="blob-code blob-code-inner js-file-line">Write a script to do the following. (Do this one part at a time, testing the partial results by inspecting the tables in SQLDeveloper, and not going on the next part until you have the previous part working.)</td>

  </tr>

  <tr>

   <td id="L13" class="blob-num js-line-number" data-line-number="13"></td>

   <td id="LC13" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L14" class="blob-num js-line-number" data-line-number="14"></td>

   <td id="LC14" class="blob-code blob-code-inner js-file-line">1. Define the following database, representing hotels, travelers who may stay in the hotels, and reservations that the travelers make at hotels.</td>

  </tr>

  <tr>

   <td id="L15" class="blob-num js-line-number" data-line-number="15"></td>

   <td id="LC15" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L16" class="blob-num js-line-number" data-line-number="16"></td>

   <td id="LC16" class="blob-code blob-code-inner js-file-line">TRAVELER(ID, FirstName, LastName, Phone)</td>

  </tr>

  <tr>

   <td id="L17" class="blob-num js-line-number" data-line-number="17"></td>

   <td id="LC17" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L18" class="blob-num js-line-number" data-line-number="18"></td>

   <td id="LC18" class="blob-code blob-code-inner js-file-line">HOTEL(ID, HotelName, City)</td>

  </tr>

  <tr>

   <td id="L19" class="blob-num js-line-number" data-line-number="19"></td>

   <td id="LC19" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L20" class="blob-num js-line-number" data-line-number="20"></td>

   <td id="LC20" class="blob-code blob-code-inner js-file-line">RESERVATION(TravelerID, HotelID, StartDate, EndDate, Confirmation)</td>

  </tr>

  <tr>

   <td id="L21" class="blob-num js-line-number" data-line-number="21"></td>

   <td id="LC21" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L22" class="blob-num js-line-number" data-line-number="22"></td>

   <td id="LC22" class="blob-code blob-code-inner js-file-line">Traveler IDs should be exactly nine characters long, hotel IDs should be exactly four characters long, and phone numbers should be exactly ten characters long; reservation confirmation codes should be at most ten characters long. You may decide on appropriate maximum lengths for names of customers, hotels, and cities.</td>

  </tr>

  <tr>

   <td id="L23" class="blob-num js-line-number" data-line-number="23"></td>

   <td id="LC23" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L24" class="blob-num js-line-number" data-line-number="24"></td>

   <td id="LC24" class="blob-code blob-code-inner js-file-line">Define the primary keys as indicated in the schemas above. Also define TravelerID in RESERVATION to be a foreign key referencing ID in TRAVELER, and HotelID in RESERVATION to be a foreign key referencing ID in HOTEL. (Thus you will have to create TRAVELER and HOTEL before RESERVATION.) We can’t assume that the confirmation codes are unique, since they are supplied by the hotels when reservations are made we can’t be sure that different hotels won’t use the same codes. (All of the confirmation codes supplied by a single hotel will be distinct, but verifying that would require a more complicated constraint than we can implement right now…)</td>

  </tr>

  <tr>

   <td id="L25" class="blob-num js-line-number" data-line-number="25"></td>

   <td id="LC25" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L26" class="blob-num js-line-number" data-line-number="26"></td>

   <td id="LC26" class="blob-code blob-code-inner js-file-line">In order to avoid conflicts, start your script file with DROP TABLE commands for all three tables (since RESERVATION contains foreign keys, you will have to drop it first). Run your script and look at the columns and constraints of each table to verify that they have been created correctly. Now you can set up trips for yourself and a couple of your friends…</td>

  </tr>

  <tr>

   <td id="L27" class="blob-num js-line-number" data-line-number="27"></td>

   <td id="LC27" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L28" class="blob-num js-line-number" data-line-number="28"></td>

   <td id="LC28" class="blob-code blob-code-inner js-file-line">2. Populate the HOTEL table with names and cities of at least four actual hotels anywhere in the world (you can make up the IDs, as they are internal to the database). Then populate the TRAVELER table with information for yourself and at least two of your friends. (For privacy reasons, IDs and phone numbers should be made up.) Look at the data in each table to verify that they have been populated correctly.</td>

  </tr>

  <tr>

   <td id="L29" class="blob-num js-line-number" data-line-number="29"></td>

   <td id="LC29" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L30" class="blob-num js-line-number" data-line-number="30"></td>

   <td id="LC30" class="blob-code blob-code-inner js-file-line">3. Next, insert at least five records to the RESERVATION table. There should be at least one record for each traveler, and at least one traveler should have two or more records in the RESERVATION table. Be sure that each traveler is staying at only one hotel at a time – that is, a traveler’s reservation at a second hotel can’t begin before their previous reservation at the first hotel ends. (This particular constraint – insuring that reservations do not overlap – is also too complicated for us to implement right now.) Every record in RESERVATION must have a starting date, but the ending date can be NULL for the traveler’s last reservation in the table. Look at the data in the table to verify that it has been populated correctly.</td>

  </tr>

  <tr>

   <td id="L31" class="blob-num js-line-number" data-line-number="31"></td>

   <td id="LC31" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L32" class="blob-num js-line-number" data-line-number="32"></td>

   <td id="LC32" class="blob-code blob-code-inner js-file-line">4. Display the contents of each table by adding commands of the form SELECT * FROM TABLENAME ; to the end of your script file. Run the complete script and save the complete contents of the output window to a text file. (Clear the window before running the script for the last time so that only the output of the last run of the script is displayed and saved.)</td>

  </tr>

  <tr>

   <td id="L33" class="blob-num js-line-number" data-line-number="33"></td>

   <td id="LC33" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L34" class="blob-num js-line-number" data-line-number="34"></td>

   <td id="LC34" class="blob-code blob-code-inner js-file-line">5. Include a comment at the top of your script file giving your name, the course number and your section number, the assignment number, and the date of submission, e.g.:</td>

  </tr>

  <tr>

   <td id="L35" class="blob-num js-line-number" data-line-number="35"></td>

   <td id="LC35" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L36" class="blob-num js-line-number" data-line-number="36"></td>

   <td id="LC36" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

 </tbody>

</table>