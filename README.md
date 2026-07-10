# ml-02-features

[![Workflow Guide](https://img.shields.io/badge/Pro--Guide-pro--analytics--02-green)](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
[![Python 3.14](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](./pyproject.toml)
[![MIT](https://img.shields.io/badge/license-see%20LICENSE-yellow.svg)](./LICENSE)

> Professional Python project: engineering and selecting features for machine learning.

## Project Description

In this project, I practiced turning raw data into better model inputs.
I focused on feature engineering and feature selection because those steps
have a big impact on model quality.

For this phase, I used the provided example workflow to:

- inspect data quality
- build useful derived features
- run a model end-to-end
- verify results with logs and executed notebook output

This helped me connect course concepts to a real, repeatable workflow.

## Example Notebook + Your Notebook

Keep the example notebook as it is.
Either copy it or use it to build a new notebook that ends in _yourname.
See [docs/your-files.md] for more.

Links:

- [ml_02_case.ipynb](notebooks/ml_02_case.ipynb)
- [ml_02_crews.ipynb](notebooks/ml_02_crews.ipynb)
- [ml_02_crews_ran.ipynb](notebooks/ml_02_crews_ran.ipynb)
- [ml_02_crews_ran.html](notebooks/ml_02_crews_ran.html)

## How I Ran the Examples

I ran the app and notebook examples from the project root folder using these commands:

```shell
uv run python -m mlstudio.app_case
uv run jupyter nbconvert --to notebook --execute notebooks/ml_02_case.ipynb --output ml_02_case_ran.ipynb
uv run jupyter nbconvert --to html notebooks/ml_02_case_ran.ipynb --output ml_02_case_ran.html
uv run jupyter nbconvert --to notebook --execute notebooks/ml_02_crews.ipynb --output ml_02_crews_ran.ipynb
uv run jupyter nbconvert --to html notebooks/ml_02_crews_ran.ipynb --output ml_02_crews_ran.html
```

After confirming success, I saved and uploaded my results:

```shell
git add -A
git commit -m "Run Phase 1 examples and add execution artifacts"
git push origin main
```

## Example Results

From my app run, I got these results:

- dataset loaded: 10 rows, 6 columns
- missing values: 0
- duplicate rows: 0
- model: LinearRegression
- mean absolute error: 0.48
- R-squared: 1.00
- predicted score for sample case: 83.4

Evidence files created by my run:

- `project.log`
- `notebooks/ml_02_case_ran.ipynb`
- `notebooks/ml_02_case_ran.html`

## What I Learned and Next Steps

What I learned:

- feature engineering changes what a model can learn
- clean, readable logs make troubleshooting much easier
- reproducible commands are important for sharing and grading

Next steps I want to take:

- run the same workflow on a different dataset
- compare performance before and after adding engineered features
- add a short discussion of which features helped most and why

## Working Files

You'll work with these areas:

- **data/raw** - raw data for exploration (only if you add a dataset)
- **docs/** - project narrative and documentation
- **src/mlstudio/** - the app is an example; run only (no need to modify)
- **notebooks/** - interactive analysis
- **pyproject.toml** - update authorship & links
- **zensical.toml** - update authorship & links

## Instructions (pro-analytics-02)

Follow the
[step-by-step workflow guide](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to complete:

1. Phase 1. **Start & Run**
2. Phase 2. **Change Authorship**
3. Phase 3. **Read & Understand**
4. Phase 4. **Modify**
5. Phase 5. **Apply**

## Challenges

Challenges are expected.
Sometimes instructions may not quite match your operating system.
When issues occur, share screenshots, error messages, and details about what you tried.
Working through issues is part of implementing professional projects.

## Success

After completing Phase 1. **Start & Run**, you'll have your own GitHub project,
with the example notebook executed and committed,
and running the example module will print out:

```shell
========================
Executed successfully!
========================
```

A new file `project.log` will appear in the root project folder.

## Command Reference

<details>
<summary>Show command reference</summary>

### In a machine terminal (open in your `Repos` folder)

After you get a copy of this repo in your own GitHub account,
open a machine terminal in your `Repos` folder:

```shell
# Replace username with YOUR GitHub username.
git clone https://github.com/Angie-Crews/ml-02-features

cd ml-02-features
code .
```

### In a VS Code terminal

These are listed for convenience.
For best results, follow the detailed instructions in
[pro-analytics-02 guide](https://denisecase.github.io/pro-analytics-02/).

```shell
uv self update
uv python pin 3.14
uv lock --upgrade
uv sync --extra dev --extra docs --upgrade

uvx pre-commit install
uvx pre-commit autoupdate

git add -A
uvx pre-commit run --all-files
# repeat if changes were made
uvx pre-commit run --all-files

# run the example module to verify the environment (.venv/)
uv run python -m mlstudio.app_case

# run common chores
uv run ruff format .
uv run ruff check . --fix
uv run python -m pyright
uv run python -m pytest
uv run python -m zensical build

# save progress
git add -A
git commit -m "update"
git push -u origin main
```

</details>

## Notes

- Use the **UP ARROW** and **DOWN ARROW** in the terminal to scroll through past commands.
- Use `CTRL+f` to find (and replace) text within a file.
- You do not need to add to or modify `tests/`. They are provided for example only.
- Many files are silent helpers. Explore as you like, but nothing is required.
- You do NOT need to understand everything; understanding builds naturally over time.

## Troubleshooting >>>

If you see something like this in your terminal: `>>>` or `...`
You accidentally started Python interactive mode.
It happens.
Press `Ctrl+c` (both keys together) or `Ctrl+Z` then `Enter` on Windows.

## Example Output (Can Remove this Section after You Verify)

```shell
| INFO | ML | Summarize workflow........
| INFO | ML | ========================
| INFO | ML | SUMMARY
| INFO | ML | ========================
| INFO | ML | Dataset: hours_scores_case
| INFO | ML | Original rows: 10
| INFO | ML | Clean rows: 10
| INFO | ML | Features: ['hours_studied', 'practice_quizzes', 'attendance_pct', 'sleep_hours', 'prior_score']
| INFO | ML | Target: score
| INFO | ML | ----- in a script, call plt.show() once at the end to display all charts -----
| INFO | ML | ----- in a script, CLOSE the chart windows with the close button to CONTINUE -----
| INFO | ML | Workflow complete
| INFO | ML | IMPORTANT: This script creates chart windows.
| INFO | ML | Close chart windows and terminate this process with CTRL+c as needed.
| INFO | ML | ========================
| INFO | ML | Executed successfully!
| INFO | ML | ========================
```

## Findings and Visuals

Take screenshots of your charts and provide them here with a discussion.
In Markdown, display a figure by using:
an exclamation mark immediately followed by square brackets containing a useful caption
immediately followed by parentheses containing the relative path to your figure.
Note: When you start typing the path with a dot (.) for "here, in this directory",
the IDE may help complete the path.

In your custom project, follow this example, but

- your figures and narrative should reflect your work,
- this `README.md` should include your commands, process, and visuals, and
- `docs/index.md` should include your narrative.

Remove unnecessary instructional comments in your custom files.

Update figures to present interesting results from your custom project:

![Provide a Useful Caption](./docs/images/Figure_1.png)

![Provide a Useful Caption](./docs/images/Figure_2.png)

## Project Documentation

Additional project instructions, terms, and notes:

[docs/index.md](docs/index.md)

## Citation

[CITATION.cff](./CITATION.cff)

## License

[MIT](./LICENSE)
