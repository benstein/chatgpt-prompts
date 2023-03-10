# ChatGPT Prompts for Productivity
Much of the discourse around ChatGPT has been (a) how amazingly magical it is, (b) novel things you can do with it, (c) future technology developments, (d) implications for search, and (e) existential impacts on humanity.

While all of that is true and interesting, it neglects that ***we all have a new tool in our toolbelt***. For me, ChatGPT sits alongside Excel, Google, my IDE, the CLI, etc as one of the ways I get work done in 2023.

But we all need to figure out the _use cases where this tool will be powerful_. Once you get past "compose an email", they're not always obvious! 

This repository hopes to inspire that. It's a collection of prompts that made ME more productive during my days. The examples herein are obviously _very_ specific to me -- that's not the point. Your takeaway should be "Oh! Wow! I never thought about using GPT to solve a problem like that!"

---

## Prompt
> I want to share examples with friends and colleagues so they can get better at using ChatGPT as a productivity tool. I will save examples on github. Write the README.md file introducing this idea

## Response
> This repository contains examples of how to use ChatGPT to increase productivity in various tasks. The examples include extracting specific information from large text files, summarizing long articles, generating ideas for brainstorming sessions, and much more.

---

## Prompt
> extract the names of venture capital firms from this blob of HTML. print them in a table. 
```
<div class="container">        <div class="row text-color-1">            <div class="col-12">                <h6 class="font-weight-bold"> List of the Largest Venture Capital Funds </h6>            </div>            <div class="col">                <span id="results-text" class="font-italic"> 273 results.. </span>            </div>            <div class="col text-right">                    <div class="btn-group">        <button type="button" class="btn btn-link btn-custom btn-small dropdown-toggle text-color-1 pointer font-weight-bold" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">            <i class="far fa-list-alt"> </i> Sort        </button>        <div class="dropdown-menu dropdown-menu-right" id="sort-dropdown">                  <li class="no-list d-pad-small"> <a href="/funds/greenspring-associates" class="text-color-1"> <i class="fas fa-user-tie fa-fw r-pad-small"></i>Greenspring Associates | $7B </a> </li>            <li class="no-list d-pad-small"> <a href="/funds/institutional-venture-partners" class="text-color-1"> <i class="fas fa-user-tie fa-fw r-pad-small"></i>Institutional Venture Partners | $7B </a> </li>            <li class="no-list d-pad-small"> <a href="/funds/andreessen-horowitz" class="text-color-1"> <i class="fas fa-user-tie fa-fw r-pad-small"></i>Andreessen Horowitz | $7B </a> </li>            <li class="no-list d-pad-small"> <a href="/funds/ggv-capital" class="text-color-1"> <i class="fas fa-user-tie fa-fw r-pad-small"></i>GGV Capital | $6.2B </a> </li>                    </ul>            </div>        </div>    </div>
```


## Response

> ---
> | Venture Capital Firms | 
> | :--------------------: |
> | Bain Capital            |
> | General Atlantic       |
> | Hillhouse Capital Group|
> | Insight Venture Partners|
> | Iconiq Capital          |
> | Andreessen Horowitz     |
> ---

---

## Prompt
Print a json blob representing 2 electrical panels that I can use for a test case

## Response
```
{
  "electrical_panels": [
    {
      "panel_id": 1,
      "manufacturer": "Siemens",
      "model": "P4",
      "num_circuits": 20,
      "voltage_rating": 240,
      "phase_type": "single",
      "panel_location": "basement"
    },
    {
      "panel_id": 2,
      "manufacturer": "Square D",
      "model": "QO",
      "num_circuits": 30,
      "voltage_rating": 240,
      "phase_type": "three",
      "panel_location": "garage"
    }
  ]
}
```

---

## Prompt
> What does this code do: Math.floor(new Date(new Date().setFullYear(new Date().getFullYear() - 1)).getTime() / 1000)

## Response
> This code calculates the Unix timestamp (the number of seconds that have elapsed since January 1, 1970, at 00:00:00 UTC) for a date that is exactly one year before the current date.
> 
> Here's a breakdown of how the code works:
> 
> 1. new Date() creates a new Date object representing the current date and time.
> 1. new Date().getFullYear() gets the year of the current date.
> 1. new Date().getFullYear() - 1 subtracts 1 from the current year, resulting in the year that is exactly one year before the current date.
> 1. new Date(new Date().setFullYear(new Date().getFullYear() - 1)) creates a new Date object representing the date that is exactly one year before the current date.
> 1. .getTime() gets the Unix timestamp (in milliseconds) for the date calculated in step 4.
> 1. / 1000 divides the Unix timestamp by 1000 to convert it from milliseconds to seconds.
> 1. Math.floor() rounds down the result of step 6 to the nearest integer.
> 
> Overall, this code is a way to get the Unix timestamp for a date that is one year before the current date, rounded down to the nearest second.

## Prompt
> Optimize it

## Response
> Here is an optimized version of the code:
> ```
> Math.floor((Date.now() - 31536000000) / 1000)
> ```
> Overall, this optimized code is more concise and performs the same calculation as the original code.

---

## Prompt
(Editor's Note: I'm not sure the use case for this, but I thought it was interesting)

> Guess the likely Indian people from this list based on their names. print them in an alphabetized bullet list: Sharan Narang, Jacob Devlin, Maarten Bosma, Aakanksha Chowdhery, Gaurav Mishra, Adam Roberts, Paul Barham, Hyung Won Chung, Charles Sutton, Sebastian Gehrmann

## Response
> Based on their names, the likely Indian people from the list are:
> - Aakanksha Chowdhery
> - Gaurav Mishra

---

## Prompt
> i have a text file and i want to find all the rows that contain the phrase “exception” (case insensitive), sort them by date, and remove duplicates.  then i want to put that into a csv file. what’s the unix command to do that?

## Response
> Here's a Unix command that should accomplish the task you've described:
> ```
> grep -i "exception" file.txt | sort -t$'\t' -k3 | awk '!a[$1,$2,$3]++' | sed 's/\t/,/g' > output.csv
> ```
> This command assumes that your input file is in a specific format with tab-separated fields, and that the date information is in the third field. If your file is in a different format, you may need to adjust the command accordingly.



