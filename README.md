# queue-using-stacks
void StackQueue :: push(int x)
{
    // Your Code
    while(!s1.empty())
    {
        s2.push(s1.top());
        s1.pop();
    }
    s1.push(x);
    while(!s2.empty())
    {
        s1.push(s2.top());
        s2.pop();
        
    }
}
//Function to pop an element from queue by using 2 stacks.
int StackQueue :: pop()
{
        // Your Code     
        int ans;
        if(!s1.empty())
        {
            ans=s1.top();
            s1.pop();
            
        }
        else{
            ans=-1;
        }
        return ans;
}
