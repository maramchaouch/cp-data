ALGORITHM somme
VAR
    a=array_tab1 : ARRAY_OF INTEGER[3,1,7,9];
    b=array_tab2 : ARRAY_OF INTEGER[2,4,1,9,3];
    i,j=INTEGER;
    test=BOOLEAN;
    so$um:=0;
BEGIN
    
    FOR i FROM 0 TO long(a) STEP 1  DO
        test=False
        FOR j FROM 0 TO long(b) STEP 1  DO
            IF (a[i]==b[j]) THEN
                test=true
            END_IF
            IF (test=False) THEN
                sum=som+a[i]
            END_IF
        END_FOR
    END_FOR
    FOR i FROM 0 TO long(b) STEP 1  DO
        test=False
        FOR j FROM 0 TO long(a) STEP 1  DO
            IF (a[j]==b[i]) THEN
                test=true
            END_IF
            IF (test=False) THEN
                sum=som+b[i]
            END_IF
        END_FOR
    END_FOR
    write(som)
END