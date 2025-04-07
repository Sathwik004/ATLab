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
