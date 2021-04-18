CS 300 Final Quiz 2021
======================

Please place all the answers for your quiz in this file.
Please do not place your name anywhere in this file.

Question 1A:
------------

Answer:

Question 1B:
------------

1.
2.
3.
4.

Question 1C:
------------

1.
2.
3.
4.

Question 2A:
------------

1.
2.

Question 2B:
------------

1.
2.
3.
4.
5.
6.

Question 3A:
------------

1.
2.

Question 3B:
------------

Answer:

Question 4A:
------------

Answer:

Question 4B:
------------

Bug 1:
Bug 2:

Fixed code:
```
ssize_t bbuffer::write(const char* buf, size_t sz) {
    std::unique_lock guard(this->mutex_);
    assert(!this->write_closed_);
    while (this->blen_ == bcapacity) {
      // wait for space to free up
    }
    size_t pos = 0;
    while (pos < sz && this->blen_ < bcapacity) {
        this->bbuf_[this->blen_] = buf[pos];
        ++this->blen_;
        ++pos;
    }
    if (pos == 0 && sz > 0) {
        return -1;
    } else {
        return pos;
    }
}
```

Question 5A:
------------

1.
2.
3.

Question 5B:
------------

1.
2.

Question 6A:
------------

1.
2.
3.
4.

Question 6B:
------------

Answer:

Question 6C:
------------

Answer:

Question 6D:
------------

Answer.

Question 6E:
------------

Answer:

Question 7A:
------------

Answer:

Question 7B:
------------

Answer:

Question 7C:
------------

Answer:
