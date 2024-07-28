# MY PROCESS

After launching the instance, we are provided with a file named `imp.red` and a remote connection.

After reading the hint, basically we just have to make sure that we are going to lose in order to get the flag.

## SOLVING

Reading the `imp.red` file will give you this:

![image](https://github.com/user-attachments/assets/97728bf3-f53c-4cb0-94da-80fcf56abb2d)

And then I tried connecting with the provided connection and this happens:

![image](https://github.com/user-attachments/assets/e6f39d67-7749-452b-8952-dcfab93e31b1)

As we can see that warrior1 must lose all rounds.

So I edited something on the `imp.red` file by just changing `mov 0, 1` into `mov 1, 1`.

![image](https://github.com/user-attachments/assets/02e5cf47-f32b-43ba-b9d9-958d47c5c158)

And somehow connecting again, it worked.

![image](https://github.com/user-attachments/assets/30e4c7ea-7266-4f07-9e15-ee7beca0fe4e)

The flag is below `You did it!`. <sub>the flag is corny as hell...<sub/>
