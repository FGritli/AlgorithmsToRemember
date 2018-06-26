# AlgorithmsToRemember

   <em>"Algorithm is a word used by programmers when they don't want to explain what they did!"</em>

Proof is a method of establishing truth, the precise meaning depends heavily on the field of study, hence it differs from one system to another. In computer science algorithm is a number of steps or a process put to achieve a specific and precise result.<hr>

There are numbers of steps used to produce functional and efficient algorithms.

-Model the problem: understand exactly why it is needed to solve the problem and what effect it will have on the program.

-Find an algorithm to solve it. Always ask if it is fast enough? How will it impact the memory?

-Find a way to address the problem. 

-Iterate until satisfied.

Most of the Algorithms and exercises I will be posting here could be used as a study guide before an interview or for computer science  exams or may be for fun.

***********Fibonacci Numbers***********

public class FibonacciNumbers {
    /*  Use of recursion, good idea but slow
        By drawing the Tree it becomes apparent that the computation is very
        repetitive T(n)>F(n) */
   
   private static int fib(int n){
        if (n <=1)
            return n;
            else
                return fib(n-1)+fib(n-2);
    }


    private static int fibFast(int m) {

        int fibFast[] = new int[m + 2];
        int i;

        fibFast[0] = 0;
        fibFast[1] = 1;

        for (i = 2; i <= m; i++) {

            fibFast[i] = fibFast[i - 1] + fibFast[i - 2];
        }

        return fibFast[m];
    }
    public static void main(String args[]) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        System.out.println(fib(n));

        int m = scanner.nextInt();
        System.out.println(fibFast(n));

    }
}
