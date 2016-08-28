# Ingredients

Brain dump of questions and ideas in no particular order. Or simply stated, a verbose README.

## CLI Interface

### Command name
What will the command/binary name be? (e.g. `git`, `npm`)
- `lager`
- `lg`
- `bl`
- `blg`

> **@bmallred**: Mmm... lager.

### Lager initiation
How does backlager get initialized? Maybe stick to similiar `git` commands?
- `backlager init --hops`

> **@bmallred**: Sounds good. What is the flag --hops intended for?

### File Type Ingestion
Backlager will be file agnostic as long as there's a `reader` for it. Examples
- .json
- .md
- .yaml
- .toml
- .xml (yes, gross but many people like to torture themselves)
- .ini
- .txt (This maybe reflects a customized lager specifc format?)

> **@bmallred**: I'm leaning that way. Thinking of tackling ```.md``` first and then just widdling away

Should we have a 'lager' format? `deployment_script_32.hops`

> **@bmallred**: Ha, why not? If they don't use it then so be it!

### Artifact Preview
Should backlager be able to generate a **local** static web application containing all artifacts so that users can view them? 
- `backlager serve`
- `backlager serve --filename file1, file2`

> **@bmallred**: Yes. I think this would go a long way for adoption b/c:
>   1. some people don't like command line
>   2. some people like pretty
>   3. and, people would not need to utilize a SaaS just to get work done.
>
> It also has the added benefit of working when there is no internet connection.


## Web Interface

### Lagerdoc Reader
- Same concept as `godoc.org`. Web interface should read in those files and render on a site

## Questions people may ask
#### How do you handle security?
- Given the distributed and flexible nature of backlager, the onus is on the users to develop a security plan. 
   - What if users want to control permissions?
   
#### How are users notified of updates to backlog items?
#### How do users subscribe to backlog item updates?
   

