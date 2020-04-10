# Duplicate-encoder-JavaScript
/*the first way that came to mind was to start by counting
all of the letters (putting the counts in an object), then
map each letter based on its count. That way you only loop
through the original word exactly twice*/
function duplicateEncode(word){
var letterCount ={};
var letters = word.toLowerCase().split('');
letters.forEach(function(letter){
letterCount[letter] = (letterCount[letter] || 0) + 1;
});
return letters.map(function(letter){
return letterCount[letter] === 1? '(' : ')';
}).join('');
}
