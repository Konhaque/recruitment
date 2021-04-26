# 2. Add Two Numbers

You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Input: (2 -> 4 -> 3) + (5 -> 6 -> 4)
Output: 7 -> 0 -> 8

function sumNumbers(numbers1,numbers2){
    var sums = [];
    var resto = 0;
    for(var i = 0; i<numbers1.length;i++){
        var sum = numbers1[i]+numbers2[i]+resto;
        if(sum >= 10){
        sum = sum+"";
        resto = parseInt(sum[0]);
        sum = parseInt(sum[1]);
        }else resto = 0;
        sums.push(sum);
    }
return sums;

}

sumNumbers([2,4,3],[5,6,4]);
