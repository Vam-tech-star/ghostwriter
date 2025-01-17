# Update AppStream Metadata

This document outlines the steps taken to update the AppStream metadata for the Ghostwriter project.

## Steps

1. **Fetch the Latest Metadata**
   - Ensure you have the latest metadata files from the AppStream repository.
     ```sh
     git fetch origin
     git pull origin master
     ```

2. **Modify the Metadata**
   - Open the relevant metadata file (e.g., `appdata.xml`) and update the necessary information. This might include:
     - Application version
     - Release notes
     - New features or bug fixes

3. **Validate the Metadata**
   - Use the AppStream CLI tool to validate the metadata.
     ```sh
     appstreamcli validate path/to/appdata.xml
     ```

4. **Commit the Changes**
   - Commit the updated metadata file to the repository.
     ```sh
     git add path/to/appdata.xml
     git commit -m "Update AppStream metadata for version X.Y.Z"
     git push origin master
     ```

5. **Create a Release**
   - Create a new release on GitHub with the updated version number and release note

```xml
<?xml version="1.0" encoding="UTF-8"?>
<component type="desktop-application">
  <id>com.example.Ghostwriter</id>
  <metadata_license>CC0-1.0</metadata_license>
  <project_license>GPL-3.0-or-later</project_license>
  <name>Ghostwriter</name>
  <summary>Text editor for Markdown</summary>
  <description>
    <p>Ghostwriter is a text editor for Markdown, providing a distraction-free writing environment.</p>
  </description>
  <release version="X.Y.Z" date="2025-01-17">
    <description>
      <p>New features and bug fixes:</p>
      <ul>
        <li>Feature 1</li>
        <li>Feature 2</li>
        <li>Bug fix 1</li>
      </ul>
    </description>
  </release>
</component>
