# Advanced search query syntax

## Notation

| Purpose | Notation |
| :--- | :--- |
| Lemma | `[LEMMA]` |
| Part-of-speech | `{POS}` |
| Surface + Part of Speech | `SURFACE{POS}` \(no space in-between\) |
| Lemma + Part of Speech | `[LEMMA]{POS}` \(no space in-between\) |
| Logical Disjunction \(OR\) | `A\|B` |
| Segment Onset \(Beginning\) | `^` |
| Negative Match | `-` |
| Wild Card \(matches exactly one word\) | `-_` |
| Wild Card \(matches multiple words\) | `*` |

## Examples

| Example | Possible Matches |
| :--- | :--- |
| `[excite]` | _excite, excites, excited, exciting_ |
| `{n}` | nouns of any kind \(except for pronouns\) |
| `{v}` | verbs of any kind |
| `to * surprise` | _to our surprise, to his surprise,_ etc. |
| `[read] {DT} [news\|paper\|article]` | _they read these articles, reading the paper or something, I'm reading the news at six,_ etc. |
| `^ having {v}` | _Having started the process, Having said that,_ etc. |
| `[help]{n}` | an aunt offered financial _help_, we called people for _help_, etc. |
| `[help]{v} {p} {v}` | _helped us build_, _help you keep_ away, _helps me understand_, etc. |
| `[get] -rid of` | _get outside of, get ahead of, got tired of,_ etc. |

