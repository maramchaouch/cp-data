ALGORITHM vectors
VAR
    v1=array_vector1 : ARRAY_OF INTEGER[1,0,0][0,1,0];
    v2=array_vector2 : ARRAY_OF INTEGER[0,1,0][1,1,1];
BEGIN
   FOR i FROM 0 TO long(v1)STEP 1  DO
    FOR j FROM 0 TO long(v1) STEP 1 DO
        res1=v1[i][j]*v1[i][j]
        j+=1
   END_FOR
     i+=1
    END_FOR
   FOR i FROM 0 TO long(v2) STEP 1  DO
   FOR j FROM 0 TO long(v2) STEP 1  DO
     res2=v2[i][j]*v2[i][j]
        j+=1
   END_FOR
   i+=1
   END_FOR

      IF (res1*res2==0) THEN
    write('the vectors are orthogonal')
    ELSE
        write('the vectors aren t orthogonal')
    END_IF
   
END