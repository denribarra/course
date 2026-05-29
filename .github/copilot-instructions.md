# Copilot Instructions for dbt Bootcamp Student Repository

This repository is designed for students following Udemy's Complete dbt Bootcamp. It is a minimal, student-focused dbt project with resources for local and Codespaces-based development.

## Project Structure
- `pyproject.toml`: Python dependencies for dbt and related tools. No `dbt_project.yml` or SQL models are included by default.
- `_course_resources/`: Contains Markdown resources, example profiles, and data location guides. Not required for running dbt.
- `README.md`: High-level setup instructions for students.

## Key Workflows
- **Environment Setup:**
  - Use Python 3.10–3.13.
  - Install dependencies with `pip install -r requirements.txt` or use `pyproject.toml` with a tool like `uv` or `pip`.
  - Codespaces users have a pre-configured environment.
- **dbt Usage:**
  - Students are expected to add their own `dbt_project.yml`, models, and profiles as part of the course.
  - Example profiles are in `_course_resources/EXAMPLE-profiles.yml`.
- **No Build/Test Automation:**
  - There are no custom build scripts, Makefiles, or test runners. All workflows are manual and course-driven.

## Conventions & Patterns
- **Minimal Starter:**
  - The repo intentionally omits models and configuration to let students build from scratch.
  - No custom folder structure or advanced dbt patterns are present.
- **Resource Directory:**
  - `_course_resources/` is for reference only; do not treat it as part of the active dbt project.

## Integration Points
- **dbt:**
  - Core dependency is `dbt-core` (see `pyproject.toml`).
  - Example for Snowflake (`dbt-snowflake`) is included, but students may add other adapters as needed.
- **Dagster:**
  - `dagster-dbt` and `dagster-webserver` are included for advanced orchestration, but not required for basic dbt usage.

## Examples
- To add a model, create a `models/` directory and add `.sql` files as per dbt documentation.
- To configure your profile, copy `_course_resources/EXAMPLE-profiles.yml` to your `~/.dbt/profiles.yml` and edit as needed.

---

**For AI agents:**
- Do not assume the presence of dbt models or configuration files; prompt the user to create them if missing.
- Reference `_course_resources/` only for examples and documentation, not as active code.
- Focus on guiding students through standard dbt workflows and setup.
