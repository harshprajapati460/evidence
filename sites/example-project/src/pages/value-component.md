# Value Component Error Handling

```summary
select 1 as total_calls
```

Errors in the Value component are now inlined into your text instead of breaking your full page. Here's an example of an empty Value tag: <Value/> which will return an error, but will stay within your text. You can hover over the error to see an error message describing the problem.

* Empty tag: <Value/>
* Non-existent query result: <Value data=abc/> 
* Wrong query result name: <Value data={data.abc}/>
* Non-existent column: <Value data={data.summary} column=abc/>
* Non-existent row without column: <Value data={data.summary} row=20/>
* Non-existent row with correct column: <Value data={data.summary} column=total_calls row=20/>

# Value Placeholders
If you like to mock up reports before you're ready to fill in real data, you can also override the Value error with a **placeholder**. Input the text you want to use as your placeholder and it will appear in blue font with square brackets, inline with your text.

Here are a few examples of placeholders: 

<Value placeholder="Report Date"/>    

Revenue has changed by <Value placeholder="YTD sales growth"/> this year, with the largest change occuring in <Value placeholder="top country name"/> (<Value placeholder="top country YTD growth"/>).
