# Advanced search query syntax

#### Notation

<table>
  <thead>
    <tr>
      <th style="text-align:left">Purpose</th>
      <th style="text-align:left">Notation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Lemma</td>
      <td style="text-align:left"><code>[LEMMA]</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Part of Speech</td>
      <td style="text-align:left"><code>{POS}</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Surface + Part of Speech</p>
        <p>(no space in-between)</p>
      </td>
      <td style="text-align:left"><code>SURFACE{POS}</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Lemma + Part of Speech</p>
        <p>(no space in-between)</p>
      </td>
      <td style="text-align:left"><code>[LEMMA]{POS}</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Logical Disjunction (OR)</td>
      <td style="text-align:left"><code>A|B</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Segment Onset (Beginning)</td>
      <td style="text-align:left"><code>^</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Negative Match</td>
      <td style="text-align:left"><code>-</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Wild Card</p>
        <p>(matches exactly one element/word)</p>
      </td>
      <td style="text-align:left"><code>-_</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Wild Card
        <br />(matching variable length of strings)</td>
      <td style="text-align:left"><code>*</code>
      </td>
    </tr>
  </tbody>
</table>#### Examples

| Example | Possible Matches |
| :--- | :--- |
| `[excite]` | _excite, excites, excited, exciting_ |
| `{n}` | nouns of any kind \(except for pronouns\) |
| `{v}` | verbs of any kind |
| `to * surprise` | _to our surprise, to his surprise,_ etc. |
| `[read] {DT} [news|paper|article]` | _they read these articles, reading the paper or something, I'm reading the news at six,_ etc. |
| `^ having {v}` | _Having started the process, Having said that,_ etc. |
| `[help]{n}` | an aunt offered financial _help_, we called people for _help_, etc. |
| `[help]{v} {p} {v}` |  _helped us build_, _help you keep_ away, _helps me understand_, etc. |
| `[get] -rid of` | _get outside of, get ahead of, got tired of,_ etc. |

