You're absolutely right — thank you for pointing that out.

I mistakenly referred to your **COIT20248 AIMS/FreshMart** assignment, not the correct **COIT20245 Assessment 2** you're working on here.

Let me now give you the **correct step-by-step plan** based strictly on the document you uploaded:

---

## ✅ COIT20245 – Assessment 2: Python Program – Step-by-Step Guide

**Scenario**: You’re completing a Python console program for **Nemo Reef Tours**, using the **supplied file `nemo_tours.py`**. Your task is to fill in the function stubs and implement the logic without modifying the menu code.

---

### 🔧 Step 1: **Download and Review the Supplied File**

* Download the provided `nemo_tours.py` from your unit Moodle site.
* Run it to observe the existing **menu interface**.
* Do **not modify** the menu code — only complete the function stubs marked with `# TODO`.

---

### 📌 Step 2: **Set Up Your Global Data Structures**

* Define these at the top of the script:

  ```python
  PASSENGER_CHARGE = 95.50
  booking_names = []
  booking_passengers = []
  booking_count = 0
  ```

---

### 🧩 Step 3: **Implement Each Menu Option**

#### ✅ Option 1: `enter_booking()`

1. Prompt for booking name:

   * Must not be blank.
2. Prompt for number of passengers:

   * Must be numeric and ≥ 1.
3. Append both to the parallel lists.
4. Call `calculate_charge(passengers)` to compute the cost (with discount).
5. Print receipt (create a `print_receipt()` function).
6. Use `global` where needed.

---

#### ✅ Option 2: `display_bookings()`

* Display all entries using this format:

  ```python
  print("{:30s}{:<11d}${:4.2f}".format(name, passengers, charge))
  ```

---

#### ✅ Option 3: `display_statistics()`

* Calculate:

  * Max and min number of passengers and corresponding names
  * Average passengers
  * Total charges
* No `max()` or `min()` — use `if` logic manually.
* Show output to 2 decimal places.

---

#### ✅ Option 4: `search_bookings()`

* Prompt for a name.
* Case-insensitive search through `booking_names`.
* If found: show name, passenger count, and charge.
* If not found: show "`<name>` not found".

---

#### ✅ Option 5: `save_bookings()`

* Save only names and passenger counts to `bookings.csv`.
* Overwrite the file each time (`'w'` mode).
* Use this format:

  ```
  Bruce McKenzie,8
  Nick Klomp,3
  ```
* Confirm with: `"Data successfully saved to file"`.

---

#### ✅ Option 6: `read_bookings()`

* Check file existence using:

  ```python
  import os.path
  os.path.exists("./bookings.csv")
  ```
* If not found: print error.
* If found:

  * Read lines, split on `,`, and append to global lists.
  * Convert passengers from string to `int`.
  * Print: `"Data successfully read from the file"`.

---

#### ✅ Option 7: Exit

* Show exit message including student number:

  ```
  Thank you for using the Nemo Reef Tours program – s1234567
  ```

---

### 📝 Step 4: Prepare the Report (`ReportAss2.docx`)

1. **Time taken**
2. **Problems faced**
3. **Screenshots of testing**

   * Use `Alt + PrtScrn` to capture your console window.
   * Annotate if needed.
4. **Test plan**

   * Document all tested cases.
5. **Append code (text only)** in the appendix.

---

### 📤 Step 5: Submit

* Files to submit:

  * ✅ `nemo_tours.py`
  * ✅ `ReportAss2.docx`

Upload to Moodle under **Assignment 2 (30%) Submission** before **Sunday, May 25, 2025 (Week 10)**.

---

Would you like help writing specific functions (like `calculate_charge()` or `display_statistics()`)?
