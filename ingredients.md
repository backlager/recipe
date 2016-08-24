# Ingredients

Brain dump of questions and ideas in no particular order. Or simply stated, a verbose README.

## CLI Interface

### Command name
What will the command/binary name be? (e.g. `git`, `npm`)
- `lager`
- `lg`
- `bl`
- `blg`

### Lager initiation
How does backlager get initialized? Maybe stick to similiar `git` commands?
- `backlager init --hops`

### File Type Ingestion
Backlager will be file agnostic as long as there's a `reader` for it. Examples
- .json
- .md
- .yaml
- .toml
- .xml (yes, gross but many people like to torture themselves)
- .ini
- .txt (This maybe reflects a customized lager specifc format?)

Should we have a 'lager' format? `deployment_script_32.hops`

### Artifact Preview
Should backlager be able to generate a **local** static web application containing all artifacts so that users can view them? 
- `backlager serve`
- `backlager serve --filename file1, file2`


## Web Interface

### Lagerdoc Reader
- Same concept as `godoc.org`. Web interface should read in those files and render on a site

## Questions people may ask
#### How do you handle security?
- Given the distributed and flexible nature of backlager, the onus is on the users to develop a security plan. 
   - What if users want to control permissions?
   
#### How are users notified of updates to backlog items?
#### How do users subscribe to backlog item updates?
   

