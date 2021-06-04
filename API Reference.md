
[Home](https://vickieponder.github.io/Sample-Riot-Games-API-Docs/)|[Getting Started](Getting Started)|API Reference|[How to Contribute](How to Contribute) 


## API Reference

**Table of Contents**

* [Introduction](#introduction)
* [Function Header](#function-header)
* [Input Parameters](#input-parameters)
* [Sample Code](#sample-code)

## Introduction
The `find_champion` function in Python returns champion suggestions based upon champion data parameters you pass through such as name, role, and origin. 
 

## Function Header

| Name | Description |
| --------- | -------- |
| find_champion | Queries champion suggestions based upon champion data parameters you pass through such as name, role, and origin.|


## Input Parameters

| Name | Data Type | Description |
| ---------  | --------  | ----------- | 
| name       | String    | Name of the champion. |
| role       | String    | Champion's assigned class. |
| origin     | String    | The region champion originates from. |


## Sample Code

Here's the sample request to the `find_champion` function:


    def find_champion(name=None, role=None, origin=None):
      champion_suggestions = []
      for champ in champion_data:
        if name:
          if champ['name'] == name:
            return [champ]
        if role:
          if champ['role'] != role:
            continue
        if origin:
          if champ['origin'] != origin:
            continue
        champion_suggestions.append(champ)
     return champion_suggestions


Here's the sample response to the `find_champion` function:

    champion_data = [
      {
        'name': 'ahri',
        'role': 'mid lane',
        'origin': 'vastaya'
      },
      {
        'name': 'teemo',
        'role': 'top lane',
        'origin': 'bandle city'
      },
      {
        'name': 'gangplank',
        'role': 'top lane',
        'origin': 'bilgewater'
      },
      {
        'name': 'sona',
        'role': 'support',
        'origin': 'ionia'
      },
      {
        'name': 'miss fortune',
        'role': 'marksman',
        'origin': 'bilgewater'
      },
     ]




