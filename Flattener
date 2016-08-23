import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

/**
 * Flattens an array of arbitrarily nested arrays of integers into a flat array of integers.
 */
public class Flattener {

    /**
     * @param inputArray an array of Integers or nested arrays of Integers
     * @return flattened array of Integers or null if input is null
     * @throws IllegalArgumentException
     */
    public static Integer[] flattenInteger(Object[] input) throws IllegalArgumentException {

        if (input == null) return null;

        List<Integer> flatList = new ArrayList<Integer>();

        for (Object element : input) {
            if (element instanceof Integer) {
                flatList.add((Integer) element);
            } else if (element instanceof Object[]) {
                flatList.addAll(Arrays.asList(flatten((Object[]) element)));
            } else {
                throw new IllegalArgumentException("Input must be an array of Integers or nested arrays of Integers");
            }
        }
        return flatList.toArray(new Integer[flatList.size()]);
    }
}
