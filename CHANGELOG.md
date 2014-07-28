## 0.1.0

### Enhancements
- Added a `nsrr console` command that allows users to access and download datasets and files
  - Datasets can be loaded in the console environment
    - `d = Dataset.find 'shhs'`
  - Dataset files can be downloaded as well
    - `d.download`
  - The download function can include a path, method, and depth
    - **path**
      - can be `nil` to download entire dataset or a string to specify a folder
    - **method**
      - 'md5' [default]
        - Checks if a downloaded file exists with the exact md5 as the online version, if so, skips that file
      - 'fresh'
        - Downloads every file without checking if it was already downloaded
      - 'fast'
        - Only checks if a download file exists with the same file size as the online version, if so, skips that file
    - **depth**
      - 'recursive' [default]
        - Downloads files in selected path folder and all subfolders
      - 'shallow'
        - Only downloads files in selected path folder
- Added a `nsrr version` command the returns the current version of the nsrr gem
- Added testing framework to more easily add new tests for new features