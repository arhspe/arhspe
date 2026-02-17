```python
from dataclasses import dataclass
from typing import List

@dataclass
class Profile:
    name: str
    role: str
    education: str
    skills: List[str]
    focus: str

arthur = Profile(
    name="arthur pereira",
    role="systems development technician & IT support analyst",
    education="technical degree from centro paula souza",
    skills=["python", "pandas", "postgres", "mysql"],
    focus="turning data and systems into structured understanding"
)

print(f"{arthur.name} – {arthur.role}")
print(f"Education: {arthur.education}")
print(f"Focus: {arthur.focus}")
```
