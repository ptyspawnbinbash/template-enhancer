# Template Enhancer

This tool utilizes the OpenAI API to improve the description, impact, and recommendation elements of a Nuclei template.

## Requirements

The tool employs the OpenAI API, requiring an API key for access. You can conveniently store this key in your .bashrc file, for example.

```
export OPENAI_API_KEY=your-key-goes-here
```

```
pip install -r requirements.txt
```

## Usage

```
python3 enhance-template.py <path-to-nuclei-template>
```

Or bash one-liner to run the script over multiple templates.

```
$high=$(nuclei -tl -s high); for i in $(echo $high); do python3 enhance-template.py $i ; done
```
This ```$high=$(nuclei -tl -s high)``` lists nuclei templates that have high severity.

This ```for i in $(echo $high); do python3 enhance-template.py $i ; done``` loops over each file-name in variable "high" and runs the script over them.

Before:

![Before](screenshots/before.png)


After:

![After](screenshots/after.png)

