Download Link: https://assignmentchef.com/product/solved-telephone
<br>
<a href="https://www.youtube.com/playlist?list=PLhOuww6rJJNN0T5ZKUFuEDo3ykOs1zxPU" rel="nofollow">https://www.youtube.com/playlist?list=PLhOuww6rJJNN0T5ZKUFuEDo3ykOs1zxPU</a>

Write a program that randomly mutates some given text which may be given on the command line:

<pre><code>$ ./telephone.py 'The quick brown fox jumps over the lazy dog.'You said: "The quick brown fox jumps over the lazy dog."I heard : "The qu)ck brown HoN jumps over thf lazy dog."</code></pre>

Or from a file:

<pre><code>$ ./telephone.py ../inputs/fox.txtYou said: "The quick brown fox jumps over the lazy dog."I heard : "=he quick brswn fox jumps over the*[azy dog."</code></pre>

The program should accept a <code>-m</code> or <code>--mutations</code> that is a floating point number between 0 and 1 that represents a percentage of mutations to introduce:

<pre><code>$ ./telephone.py -m .5 ../inputs/fox.txtYou said: "The quick brown fox jumps over the lazy dog."I heard : "weeqhR$kBbxown|foGLFuvn| ooe: t'. l"zy d&amp;:."</code></pre>

It should also accept a <code>-s</code> or <code>--seed</code> argument for the random seed to ensure reproducible results:

<pre><code>$ ./telephone.py -s 2 ../inputs/fox.txtYou said: "The quick brown fox jumps over the lazy dog."I heard : "TheNqHick Crown fox jum_s over the lazy dog."</code></pre>

If provided no arguments, it should print a brief usage:

<pre><code>$ ./telephone.pyusage: telephone.py [-h] [-s int] [-m float] strtelephone.py: error: the following arguments are required: str</code></pre>

<pre><code>$ ./telephone.py -husage: telephone.py [-h] [-s int] [-m float] strTelephonepositional arguments:  str                   Input text or fileoptional arguments:  -h, --help            show this help message and exit  -s int, --seed int    Random seed (default: None)  -m float, --mutations float                        Percent mutations (default: 0.1)</code></pre>

Run the test suite to ensure your program is correct:

<pre><code>$ make testpytest -xv test.py============================= test session starts ==============================...collected 10 itemstest.py::test_exists PASSED                                              [ 10%]test.py::test_usage PASSED                                               [ 20%]test.py::test_bad_seed_str PASSED                                        [ 30%]test.py::test_bad_mutation_str PASSED                                    [ 40%]test.py::test_bad_mutation PASSED                                        [ 50%]test.py::test_for_echo PASSED                                            [ 60%]test.py::test_now_cmd_s1 PASSED                                          [ 70%]test.py::test_now_cmd_s2_m4 PASSED                                       [ 80%]test.py::test_fox_file_s1 PASSED                                         [ 90%]test.py::test_fox_file_s2_m6 PASSED                                      [100%]============================== 10 passed in 0.82s ==============================</code></pre>