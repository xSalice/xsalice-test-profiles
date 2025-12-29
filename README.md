# xSalice Community Profiles

Community-shared Event and Timeline profiles for xSaliceAIO.

## Repository Structure

```
events/{JobName}/profilename.json
timelines/{JobName}/profilename.json
manifest.json
```

Job folders use normalized names without spaces (e.g., `WhiteMage`, `DarkKnight`, `BlackMage`).

## manifest.json

The manifest tracks all profile versions:

```json
{
  "events/Sage/template.json": "1.0.0",
  "timelines/Sage/template.json": "1.0.0"
}
```

The client compares local versions against the manifest to detect updates.

## Profile Format

```json
{
  "Id": "unique_id",
  "Name": "Display Name",
  "Description": "What this profile does",
  "CreatedAt": "2025-12-28T00:00:00Z",
  "ModifiedAt": "2025-12-28T00:00:00Z",
  "Version": "1.0.0",
  "Entries": []
}
```

## Publishing Updates

1. Update your profile JSON
2. Increment the `Version` field
3. Update the version in `manifest.json` to match
4. Commit and push
