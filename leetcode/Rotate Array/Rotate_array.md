## 문제
- 난이도 :
- 배열이 주어지면 k번 배열을 오른쪽으로 돌립니다.(k>0)

- Example 1:
```
Input: nums = [1,2,3,4,5,6,7], k = 3
Output: [5,6,7,1,2,3,4]
Explanation:
rotate 1 steps to the right: [7,1,2,3,4,5,6]
rotate 2 steps to the right: [6,7,1,2,3,4,5]
rotate 3 steps to the right: [5,6,7,1,2,3,4]
```

- Example 2:
```
Input: nums = [-1,-100,3,99], k = 2
Output: [3,99,-1,-100]
Explanation: 
rotate 1 steps to the right: [99,-1,-100,3]
rotate 2 steps to the right: [3,99,-1,-100]
```

Constraints:

1 <= nums.length <= 10<sup>5</sup><br/>
-2<sup>31</sup> <= nums[i] <= 2<sup>31</sup> - 1<br/>
0 <= k <= 10<sup>5</sup>

### 나의 풀이
(1) 1차 풀이 - fail
```javascript
var rotate = function(nums, k) {
    nums.sort((a,b) => b-k).sort((a,b) => {if(a<0 && b<0){return b-a}})
};
```
이유 : 왼쪽으로 보낸다고 잘못 생각했다.. 오른쪽으로 한 칸씩 이동하는 것.
