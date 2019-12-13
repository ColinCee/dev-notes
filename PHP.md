### Performance

Almost always use `isset` over `array_key_exists`, similar O(n) (almost O(1)) but `isset` is still faster in the real world. However `isset` cannot differentiate uninitialised and actual null values
