# AT Lab

## Alert Dialog
AlertDialog.Builder ab = new AlertDialog.Builder(MainActivity2.this);

ab.setTitle("Darshaan");
ab.setMessage("do you really want to do this?");

ab.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
    @Override
    public void onClick(DialogInterface dialog, int which) {
        Toast.makeText(MainActivity2.this, "Thanks!", Toast.LENGTH_SHORT).show();
    }
});

ab.setNegativeButton("no", null);
<b>ab.show();</b>
});

## Button
Button button = findViewById(R.id.button);
button.setOnClickListener((v)->{
});


## Toast
Toast.makeText(MainActivity.this, "You clicked a button", Toast.LENGTH_SHORT).show();

## Intent
Intent intent = new Intent(MainActivity.this, MainActivity2.class);

intent.putExtra("name", "Sathwik");
intent.putExtra("age", 21);

startActivity(intent);

// In the other activity
String name = getIntent().getStringExtra("name");

## Something
