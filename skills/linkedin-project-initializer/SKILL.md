---
name: linkedin-project-initializer
description: "Initialize a LinkedIn marketing project workspace with an AGENT.md configuration block and default stores for connections, the Story Bank, and the voice profile. Use when the user asks to set up or scaffold a LinkedIn workspace, create its default directories, or generate its AGENT.md. Not for drafting or auditing LinkedIn content (use the matching writing or humanizer skill)."
---

# LinkedIn Project Initializer

Create the project-level files and directories that the `linkedin-marketing`
bundle reads. This skill initializes structure only. It does not interview the
user, draft content, import contacts, or fill personal data.

## When to use

- "Initialize a LinkedIn project"
- "Set up the LinkedIn workspace"
- "Create the default LinkedIn directories"
- "Generate AGENT.md for linkedin-marketing"

Not for:
- Drafting a post, comment, reply, or profile
- Building a voice profile from writing samples
- Interviewing for Story Bank material
- Migrating or importing existing connection data

## Default workspace

The default target is the current project root:

```text
<project-root>/
├── AGENT.md
├── .gitignore
└── linkedin/
    ├── connections/
    │   └── index.md
    ├── story-bank.md
    └── voice-profile.md
```

The default `AGENT.md` configuration is:

```yaml
linkedin-marketing:
  connections_dir: linkedin/connections
  story_dir: linkedin
  voice_dir: linkedin
```

This maps to:

- `CONNECTIONS_DIR` = `linkedin/connections/`
- `STORY_BANK_FILE` = `linkedin/story-bank.md`
- `VOICE_PROFILE_FILE` = `linkedin/voice-profile.md`

Do not create separate `story/` or `voice/` directories unless the user
explicitly asks for those paths.

## Steps

1. **Determine the target project root.** Use the current project root by
   default. If the user supplies a target directory, use that instead. Ask only
   when neither can be determined.

2. **Preflight the workspace.** Check whether `AGENT.md`, `.gitignore`, and
   each default file already exist. Read every existing target file before
   changing anything. Never treat this initialization as permission to replace
   personal data, stored profiles, or unrelated project instructions.

3. **Create the directories.** Create the project root if the user explicitly
   requested a new directory. Then create:
   - `linkedin/`
   - `linkedin/connections/`

4. **Create missing starter files.** Use the exact starter content in
   `references/workspace-templates.md`.
   - Create `linkedin/connections/index.md` when it is missing or empty.
   - Create `linkedin/story-bank.md` when it is missing or empty.
   - Create `linkedin/voice-profile.md` when it is missing or empty.
   - Preserve every non-empty existing file unchanged.

5. **Create or merge AGENT.md.**
   - If `AGENT.md` does not exist, create it with a short project heading and
     the default `linkedin-marketing` YAML block.
   - If it exists without a `linkedin-marketing` block, append the block while
     preserving all existing content.
   - If the same block already exists, leave the file unchanged.
   - If a different `linkedin-marketing` block already exists, do not
     overwrite it. Report the current values and ask whether to keep them or
     change them.
   - If an existing `linkedin-marketing` block is malformed, do not edit it.
     Report the problem and ask for the intended values.
   - Keep exactly one configuration block.

   When the user explicitly supplies custom store paths, write those values
   instead of the defaults. Create the configured directories and initialize
   the same fixed filenames inside them.

6. **Protect the stores with `.gitignore`.** Create `.gitignore` if missing or
   append only missing entries. By default add:

   ```gitignore
   linkedin/connections/
   linkedin/voice-profile.md
   linkedin/story-bank.md
   ```

   If AGENT.md uses custom paths, add equivalent ignore rules for those paths
   as well. Do not duplicate an existing matching rule and do not remove
   unrelated ignore rules.

7. **Validate the result.**
   - Confirm the configured directories exist.
   - Confirm `index.md`, `story-bank.md`, and `voice-profile.md` exist.
   - Confirm the Story Bank and voice profile still contain `filled: no` when
     they were newly created.
   - Confirm AGENT.md contains one valid `linkedin-marketing` block.
   - Confirm the personal stores are covered by `.gitignore`.

## Hard rules

- Be idempotent. Running the skill twice must not duplicate configuration or
  overwrite user data.
- Preserve existing `AGENT.md` instructions and non-empty store files.
- Do not put names, career details, voice samples, or private messages into the
  starter files.
- Do not fetch anything from the network or call a third-party service.
- Do not create content drafts or pretend the workspace is personalized. It is
  initialized but not filled.
- Use the exact fixed filenames `story-bank.md` and `voice-profile.md`.
- If any write fails, report the failed path and the files already created.
  Do not hide a partial initialization.

## Output

Return a concise setup report:

```text
LinkedIn project workspace: <project-root>

Created:
- <paths>

Preserved:
- <paths>

Configuration:
- connections_dir: <path>
- story_dir: <path>
- voice_dir: <path>

Validation: OK
Next: use linkedin-interviewer to fill the Story Bank or
linkedin-humanizer profile mode to build the voice profile.
```

If a conflict blocks AGENT.md, replace `Validation: OK` with
`Needs decision: <conflict>` and ask one focused question. Do not call the
workspace fully initialized while the configuration is unresolved.

## Resources

- `references/workspace-templates.md` — starter contents for AGENT.md,
  connections index, Story Bank, and voice profile
