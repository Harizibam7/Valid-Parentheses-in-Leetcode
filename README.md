# Valid-Parentheses-in-Leetcode


Valid Parentheses in LeetCode By using C++

    class Solution {
    public:
        bool isValid(string s) {
            stack<char>st;
            for(auto ch:s){
                if(ch=='('||ch=='{'||ch=='['){
                    st.push(ch);
                }else{
                   
                    if((!st.empty())&&(ch==')' && st.top()=='(' || ch=='}' && st.top()=='{' || ch==']' && st.top()=='[')){
                        st.pop();
                    }else{
                        return false;
                    }
    
                }
    
            }
           return st.empty();
        }
    };
