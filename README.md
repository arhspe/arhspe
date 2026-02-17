## Hi There! 👋

<table>
  <tr>
    <td>
      <blockquote>
          Coding things with ❤️ <br>
          <sub>
        <em>
            Feel free to reach out at <strong>arhspe.contato@gmail.com</strong>
          </sub>
        </em>
      </blockquote>
    </td>
    <td width="90" align="center">
      <img 
        src="https://github.githubassets.com/images/mona-loading-default.gif"
        width="70"
        alt="GitHub loading"
      />
    </td>
  </tr>
</table>


```python
from dataclasses import dataclass
from typing import List

@dataclass
class DataProfile:
    role: str
    stack: List[str]
    databases: List[str]
    principles: List[str]
    focus: str

arthur = DataProfile(
    role="data-focused developer",
    stack=["python", "sql"],
    databases=["postgres", "mysql"],
    principles=["clarity", "structure", "reproducibility"],
    focus="turning data into structured understanding"
)

```
