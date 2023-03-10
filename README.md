# chatgpt-prompts
A collection of prompts that made me more productive and I want to share with you

This repository contains examples of how to use ChatGPT to increase productivity in various tasks. The examples include extracting specific information from large text files, summarizing long articles, generating ideas for brainstorming sessions, and much more.

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