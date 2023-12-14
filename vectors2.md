ALGORITHM vectors
VAR
    v1=array_vector1 : ARRAY_OF INTEGER[1,0,0,1][0,1,0,1];
    v2=array_vector2 : ARRAY_OF INTEGER[0,1,0,1][1,1,1,0];
    i,j=INTEGER
BEGIN
    FOR i FROM 0 TO long(v1) STEP 1  DO
    FOR j FROM 0 TO long(v2) STEP 1  DO
        IF (dot_product(v1,v2)==0) THEN
    write('the vectors are orthogonal')
    ELSE
        write('the vectors are not orthogonals')
    END_IF
       
    END_FOR
  END_FOR
END
PROCEDURE dot_product(v1,v2)
VAR
  i,j,res1,res2,res=INTEGER
BEGIN
  FOR i FROM 0 TO long(v1) STEP 1  DO
    FOR j FROM 0 TO long(v2) STEP 1  DO
       res1=v1[0][j]*v2[0][j]
        j+=1
    END_FOR
  END_FOR
   FOR i FROM 0 TO long(v1) STEP 1  DO
    FOR j FROM 0 TO long(v2) STEP 1  DO
       res2=v1[1][j]*v2[1][j]
        j+=1
    END_FOR
  END_FOR
  res=res1*res2
END
