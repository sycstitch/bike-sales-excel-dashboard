<details>
<summary><b>Problem:</b> Pivot Table shows '###' in some cells.</summary>

**Solutions:**

- Refresh data.
- Make cells longer (happens because there’s not enough space to display numbers):
  - Select the column, right-click, choose 'Column width'.
  - Try 'Autofit' first, then 'Custom' if it reverts back.
</details>

---

<details>
<summary><b>Problem:</b> "The PivotTable field name is not valid. To create a PivotTable report, you must use data that is organized as a list with labeled columns. If you are changing the name of a PivotTable field, you must type a new name for the field."</summary>

**Solution:**  
Only select the columns with headers.

- [Source](https://stackoverflow.com/questions/63523302/the-pivottable-field-name-is-not-valid-to-create-a-pivottable-report-you-must)
- Shortcuts to save your headache:  
  - Click the first header, then Shift + Click the last header.  
  - Or use Shift + Cmd/Ctrl + Down Arrow to select entire columns.
</details>

---

<details>
<summary><b>Problem:</b> Local branch and remote <code>main</code> diverged after editing <code>README.md</code> directly on GitHub without pushing local changes first. Needed to keep local changes except for <code>README.md</code>, which should match remote.</summary>

**Solution:**

1. **Fetch remote changes:**  
   `git fetch origin`  
   *Downloads latest remote commits without merging to avoid conflicts upfront.*

2. **Replace local README.md with remote version:**  
   `git checkout origin/main -- README.md`  
   *Overwrites local README.md with remote copy while preserving other local files.*

3. **Commit local changes:**  
   ```bash
   git add .
   git commit -m "Your changes"
   ```  
   *Stages and commits all local edits to prepare for rebasing.*

4. **Rebase local commits onto remote branch:**  
   `git pull --rebase origin main`  
   *Reapplies local commits on top of updated remote history for a clean, linear commit history.*

5. **Handle uncommitted local changes blocking rebase:**

   - To **keep** changes:  
     ```bash
     git add <file>
     git commit -m "Save changes"
     git rebase --continue
     ```
   
   - To **discard** changes:  
     ```bash
     git restore <file>
     git rebase --continue
     ```
   *Ensures rebase can proceed without overwriting local edits unintentionally.*

6. **Push updated branch:**  
   `git push origin main`  
   *Uploads the rebased, updated local branch to remote.*

**Outcome:**  
Successfully synchronized local and remote branches, preserved local changes, and updated README.md to match remote without conflicts or data loss.
</details>