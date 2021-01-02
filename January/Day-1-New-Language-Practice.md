# Day 1 - Leetcode in 2 New Flavors! :ice_cream:

This year, I expect to be working with 2 languages that are completely new to me at the moment!
These two languages are: C++ and Ruby

### The context for each:
* C++  - an Operating Systems course 
* Ruby - my summer internship as a Support Engineer

Just to start learning these two, I'm doing leetcode questions in each language respectively as a way to learn!

Update: I started trying to do this at 12:30am on the next day...how naive I was to think it'd be easy to figure out even an easy Leetcode problem!

Consequently, here are the solutions I found to Leetcode 136 (Find the Single Number). These two languages feel very different to me! 

C++:
`int singleNumber(vector<int>& nums) {
    unordered_map<int,int> times;

    for(auto num : nums) times[num]++;

    unordered_map<int, int>::iterator itr;
    for(itr = times.begin(); itr != times.end(); itr++){
        if(itr->second == 1) return itr->first;
    }

    return 0;
}`

Ruby: 
`def single_number(nums)
    nums.sort!
    i = 0
    
    while i < (nums.length - 1)
    
        unless nums[i+1] == nums[i]
           return nums[i] 
        end
        i += 2
    end
    return nums[-1]
end`
