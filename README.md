# Stack-using-queue

public class Solution{
    public static class Stack {
        // Define the data members
        Queue<Integer> q= new LinkedList<Integer>();
        public Stack() {
            // Implement the Constructor.
            this.q=q;

        }

        /*----------------- Public Functions of Stack -----------------*/

        public int getSize() {
            return q.size();
            // Implement the getSize() function.
        }

        public boolean isEmpty() {
            // Implement the isEmpty() function.
            if(q.size()==0){
                return true;
            }
            else{
                return false;
            }
        }

        public void push(int element) {
            // Implement the push(element) function.
            q.add(element);
            for(int i=0;i<q.size()-1;i++){
                q.add(q.remove());
            }

        }

        public int pop() {
            // Implement the pop() function.
            if(q.isEmpty()){
                return -1;
            }
            return q.remove();
        }

        public int top() {
            // Implement the top() function.
            if(q.isEmpty()){
                return -1;
            }
            return q.peek();
        }
    }
}
