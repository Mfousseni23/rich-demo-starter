Rich Demo Starter
=================

A tiny repository that showcases the `rich`_ library for beautiful terminal output:
colors, emoji, tables, progress bars, live dashboards, and more.

Why Rich?
---------

* **Instant polish** for scripts and CLIs with almost no code changes.
* Clearer **progress reporting** and **status** indications.
* **Readable tables** for quick data inspection.
* Improved **tracebacks** that make debugging easier.

.. _rich: https://github.com/Textualize/rich

Installation
------------

You need Python 3.9+.

Option A: with ``pip`` and a virtual environment::

    python -m venv .venv
    . .venv/bin/activate  # Windows: .venv\Scripts\activate
    pip install -U pip
    pip install -e .

Option B: minimal install using ``requirements.txt``::

    python -m venv .venv
    . .venv/bin/activate
    pip install -r requirements.txt
    pip install -e .

Usage
-----

This project exposes a few console scripts via ``pyproject.toml``:

* ``rich-hello`` — basic Markdown in a panel
* ``rich-table`` — nicely formatted table
* ``rich-progress`` — spinner + progress bar with ETA
* ``rich-live`` — simple "live" dashboard that updates in-place

Run them after installation::

    rich-hello
    rich-table
    rich-progress
    rich-live

Or run modules directly without installing::

    python -m src.rich_demo.hello
    python -m src.rich_demo.table_demo
    python -m src.rich_demo.progress_demo
    python -m src.rich_demo.live_dashboard

Screenshots (what to expect)
----------------------------

* **hello**: a cyan rule, then a green-bordered panel rendering Markdown.
* **table**: a title and a 3-row leaderboard with colored columns.
* **progress**: spinner, progress bar, counts, and time remaining.
* **live**: an updating panel with random metrics (CPU, memory, req/s).

Uninstall
---------

If installed in editable mode::

    pip uninstall rich-demo-starter

Testing
-------

Run a quick import test with ``pytest``::

    pip install pytest
    pytest

Troubleshooting
---------------

* On Windows PowerShell, ensure ANSI colors are enabled (Rich handles most cases).
* If you see "command not found", your virtualenv may not be activated.

License
-------

MIT
