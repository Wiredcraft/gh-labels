# GitHub Labels

We wasted a lot of time setting up labels on GitHub every time we create a new repo. We wanted a way to just
automate that process, especially since we have a standard list of labels we use for all our projects.

This little Python script prompts you for a GitHub repository (and a GitHub token)
and set up the labels for this repo to match what you have in a [`labels.yml`](https://github.com/Wiredcraft/gh-labels/blob/master/labels.yml) file. This file includes a simple
list of label settings;

```
- name: 'Status: Backlog'
  color: 'F1F8E9'
- name: 'Status: In progress'
  color: 'AED581'
(...)
```

## Install & Run

1. Clone the repo: `git clone https://github.com/Wiredcraft/gh-labels.git`
1. Get in the folder: `cd gh-labels`
1. Create and activate your virtualenv;

        virtualenv venv
        source venv/bin/activate
        
1. Install dependencies; `pip install -r requirements.txt`
1. Run it; `python github.py`

You'll be prompted for a valid GitHub API token (see https://github.com/settings/tokens) as well as the repo name in the
`Wiredcraft/gh-labels` format.

The labels are defined in the `labels.yml` file. Modify it to fit your needs.
