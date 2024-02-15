#Input Mask for Phone Numbers

- Feb 15th, 2023 - 260+ countries patterns


##How to Use

1) Create a Page Variable with `text` data type

![Page Variable](https://github.com/gustavreinehr/appgyver/assets/75501879/55f93bbe-0e4c-4722-aa4a-17238e01e59a)

2) Bind this Page Variable to the input's value

![Input value binded to Page Variable](https://github.com/gustavreinehr/appgyver/assets/75501879/380c9c4f-9ae9-4bd5-b0df-1f21e66f0b1f)

3) Select the input, open your Logic Canvas, and add a `JavaScript` node to the `Component onChange` Event

![Logic Canvas](https://github.com/gustavreinehr/appgyver/assets/75501879/8c8f893c-13c9-4e6a-91a2-2acbb25a3483)

4) Open the `JavaScript` node and bind the Page Variable you created on Step 1 to the `input1`. Make sure to configure the `Outputs` as in the image below. Also, paste the code of the [js-code.js](./js-code.js) in place.

![JavaScript node configuration](https://github.com/gustavreinehr/appgyver/assets/75501879/bfea8a29-bde2-4734-a135-0d93b3aad21c)

5) Finally, add a `Set page variable` node after the `JavaScript` node, select the Page Variable you created on Step 1 as the **"Variable Name"** and set the **"Assigned Value"** to *Output value of another node* -> `result`.

![Set page variable node](https://github.com/gustavreinehr/appgyver/assets/75501879/d7dc3210-3821-4282-9a58-5423b107d2b2)

6) Now, as you type, the mask will be dynamically applied to your input.
